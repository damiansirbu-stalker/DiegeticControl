DiegeticControl: In-world volume control for STALKER Anomaly, by Damian
Version: 1.0.10-snapshot (xlibs 1.8.4, demonized 20250908)
Changelog: https://github.com/damiansirbu-stalker/DiegeticControl/blob/main/doc/changelog
Russian / На русском: https://github.com/damiansirbu-stalker/DiegeticControl/blob/main/doc/readme_ru.txt

My work:
GitHub: https://github.com/orgs/damiansirbu-stalker/repositories
ModDB: https://www.moddb.com/members/damian-sirbu/addons
Nexus: https://www.nexusmods.com/profile/damiansirbu/mods

My contributions:
X-Ray Monolith: https://github.com/themrdemonized/xray-monolith

[ HERO IMAGE: diegeticcontrol-hero.gif — per-source control of in-world sound ]

Anomaly has no way to control the volume of radios, megaphones, guitars, and harmonicas independently from the game's audio sliders. You can't turn down Duty propaganda without killing ambient sounds. DiegeticControl fixes this.

The mod hooks directly into the audio subsystems that play in-world sound: ph_sound for radios and megaphones, guitar_anim for campfire guitar, harmonica_anim for harmonica. Each source gets its own volume slider, enable/disable toggle, and where applicable a pause multiplier that controls silence between tracks or announcements.

A master volume multiplier sits on top of everything. All changes apply immediately through MCM.

Missing dependencies are handled gracefully. If you don't have the guitar or harmonica mods installed, those controls simply do nothing.

Features:

Radios:
  Volume control for faction base radios and music
  Pause multiplier between tracks (longer silence or shorter)
  Enable/disable toggle

Megaphones:
  Volume control for Duty propaganda, Arena announcer, alarms
  Pause multiplier between announcements
  Enable/disable toggle

Guitar:
  Volume control for campfire guitar (requires Guitar Animation mod)
  Enable/disable toggle

Harmonica:
  Volume control for harmonica (requires Harmonica mod)
  Enable/disable toggle

Master volume multiplier applied to all sources

Requirements:
Anomaly 1.5.3
Modded exes: themrdemonized 20250908 or newer, or AOEngine v0.55 or newer. The full feature set needs the latest demonized build. A feature that needs a newer one stays inactive on older exes.
xlibs (https://www.moddb.com/mods/stalker-anomaly/addons/xlibs-1001)
MCM
Radio_Remastered or similar (for radio/megaphone control)
Guitar Animation by Daiviey (optional, for guitar control)
Harmonica by Daiviey (optional, for harmonica control)

Install (MO2):
1. Install xlibs
2. Install DiegeticControl
3. Load order does not matter
4. Configure via MCM

Uninstall (MO2):
Disable or remove in MO2.

Configuration:
All settings in MCM under DiegeticControl. All defaults are 1.0 (unchanged from game behavior).

Compatibility:
Coexists with the mods it controls. It hooks ph_sound, guitar_anim, and harmonica_anim, and a control is inactive when its mod is absent.
Tested with Anomaly 1.5.3, GAMMA, and Forgotten Zone.

How It's Built:

Although it started from work by Demonized, Alundaio, and Tronex, the current code and patterns are original, learned through reverse-engineering X-Ray, load testing, and custom X-Ray changes.
The design favors the engine's own mechanisms and minimal intervention, with event-native pub/sub over polling.
Work spreads across frames through deferred queues and rate limiters, while per-level caches replace world scans.
The raycasting and range math are hand-written and tested live, and the code follows the engine's own standards and flags.
Performance is the first invariant. Every flow stays under 2ms, and the build rewrites or drops anything that misses.
Profiled continuously with JitProfiler, an engine-native scientific tool. Manual tests run on unoptimized, single-threaded exes.
The code carries tracing and monitoring from the ground up, with every flow timed off the log level.
Every commit runs the full pipeline locally and in CI: luacheck, a Selene build compiled for STALKER with flags the public build lacks, and a load test that runs every script against engine stubs.
Rule layers then check crash safety, hotpath cost, engine correctness, complexity, architecture contracts, security, and the docs.
Every mod is configurable through MCM or LTX, down to each rate, threshold, and toggle, with nothing tunable left hard-coded.
The mod avoids writing engine values, holding its own state in parallel. Any value it must change stays inside the engine's own bounds, so save corruption is impossible.
The family runs on one rulebook through xlibs. Every rule, policy, and check is one shared implementation, the same protection, distances, faction logic, and combat reads in every mod.
It depends on no other mod, not even my own. The only shared layers are X-Ray and xlibs.

[Screenshot: DiegeticControl under JitProfiler, a live CPU and allocation capture]
Project Health: https://damiansirbu-stalker.github.io/DiegeticControl/

Credits:
Altogolik - support, ideas, source materials

Usage and License:
  Modpacks: allowed and encouraged. Keep the readme and license files.
  Addons, patches, integrations: allowed. Credit "DiegeticControl by Damian Sirbu" visibly on your mod page.
  Reproducing the implementation in other software: not allowed, even with credit.
  Full license in LICENSE file and on GitHub.

Diagnostics and reporting:
Debug mode: turn on in MCM, reproduce, then off. Writes diegeticcontrol.log.
Report at https://github.com/damiansirbu-stalker/DiegeticControl/issues/new/choose or the EFP, Anomaly, and Zona Discord. Include repro steps, engine build, modlist, load order, xray.log, and the debug log.

Tags: engine-native, performance, save-safe, diegetic, audio, audio-mixer, volume-control, per-source-volume, live-control, immersion, quality-of-life
