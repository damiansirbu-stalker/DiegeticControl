Версия: 1.1.1-snapshot (xlibs 1.9.0, demonized latest)
Changelog: https://github.com/damiansirbu-stalker/DiegeticControl/blob/main/doc/changelog
Health: https://damiansirbu-stalker.github.io/DiegeticControl/health/
JitProfiler: https://damiansirbu-stalker.github.io/DiegeticControl/jitprofiler/
Bugs: https://github.com/damiansirbu-stalker/DiegeticControl/issues
English / По-английски: https://github.com/damiansirbu-stalker/DiegeticControl/blob/main/doc/readme.txt

---
Моды Alife:
  AlifePlus: https://www.moddb.com/mods/stalker-anomaly/addons/alifeplus-v1-0-01
  AlifeTactics: https://www.moddb.com/mods/stalker-anomaly/addons/alifetactics
  AlifeBalance: https://www.moddb.com/mods/stalker-anomaly/addons/alifebalance
  AlifeGuard: https://www.moddb.com/mods/stalker-anomaly/addons/alifeguard-1001
Моды Diegetic:
  DiegeticControl: https://www.moddb.com/mods/stalker-anomaly/addons/diegeticcontrol
  DiegeticAmbience
  DiegeticDread
Инструменты:
  JitProfiler: https://www.moddb.com/mods/stalker-anomaly/addons/jitprofiler
Библиотеки:
  xlibs: https://www.moddb.com/mods/stalker-anomaly/addons/xlibs-1001
Движки:
  X-Ray Monolith: https://github.com/themrdemonized/xray-monolith/pulls?q=is%3Apr+author%3Adamiansirbu+is%3Amerged
  OpenXRay: https://github.com/OpenXRay/xray-16/pulls?q=is%3Apr+author%3Adamiansirbu+is%3Amerged
  IX-Ray: https://github.com/ixray-team/ixray-1.6-stcop/commits/develop?author=damiansirbu
Зависимые моды:
  COMPASS: https://github.com/Crimento/COMPASS
  Nemesis Spawn System: https://github.com/SirEndet/Nemesis-Spawn-System
  Word of Mouth: https://www.moddb.com/mods/stalker-anomaly/addons/word-of-mouth
Интеграции:
  Warfare (erepb): https://www.moddb.com/mods/stalker-anomaly/addons/warfare-alife-overhaul-new
  Homestead: https://www.moddb.com/mods/stalker-anomaly/addons/homestead-stalker-settlement-builder
  Stealth Overhaul: https://github.com/Alex-leon1594/Stealth_Overhaul_Reworked
  TALKER: https://www.moddb.com/mods/stalker-anomaly/addons/talker-ai-powered-npc-dialogue-beta
  Factions of the Zone: https://github.com/devinhorowitz/factionsofthezone
  Anomaly Radios Extended: https://www.moddb.com/mods/stalker-anomaly/addons/anomaly-radios-extended-full-remaster-152
Сотрудничество:
  xAGNA: https://www.moddb.com/mods/stalker-anomaly/addons/xagna

[ Hero image: diegeticcontrol-hero.gif - управление громкостью каждого источника в мире ]

Мои работы бесплатны и открыты, входят в большинство модпаков и интегрируются с известными проектами.
Организованная группа копирует мои работы, клевещет на меня, выдаёт себя за меня и устраивает ревью-бомбинг на всех площадках.
Помочь можно отзывом, оценкой, грамотным баг-репортом или кофе на Ko-fi: https://ko-fi.com/damiansirbu

Каждый релиз стабилен, а новый может добавить целые системы или перенести их настройки.
После каждого обновления откройте раздел Разработка в MCM и сбросьте все настройки к значениям по умолчанию.

Регулятор громкости, которого в игре никогда не было.

DiegeticControl даёт каждому источнику звука в мире свою громкость в MCM: радио, мегафонам, а также гитаре и гармонике, на которых играете вы.
В ванили эти звуки идут за игровыми ползунками звука, и пропаганду Долга нельзя приглушить, не приглушив вместе с ней окружение.
Теперь у каждого источника свой ползунок и переключатель, и изменение применяется сразу, как только вы его двигаете.
Если аддона, который даёт источник, нет, его регуляторы просто бездействуют, и ничего не ломается.

Возможности:

Общая громкость:
  Один множитель для всех источников на странице.
  Он также масштабирует все остальные скриптовые звуки мира, которые игра проигрывает через ту же звуковую систему.

Радио:
  Радио на базах, у торговцев и в лагерях, и музыка, которую они играют, на вашей громкости.
  Пауза между треками растягивается или сокращается, а на значении 1.0 возвращается исходный ритм.
  Выключенные, все радио молчат.

Мегафоны:
  Пропаганда Долга, диктор Арены, тревоги и объявления, на своей громкости.
  Пауза между объявлениями растягивается или сокращается так же.
  Выключенные, все мегафоны молчат.

Гитара:
  Гитара, на которой играете вы сами, из аддона Guitar Animation от Daiviey, на своей громкости.
  Она играет случайный трек из аддона, а выключенная не играет ничего.

Гармоника:
  Губная гармоника, на которой играете вы сами, из аддона Harmonica от Daiviey, на своей громкости.
  Она играет случайный трек из аддона, а выключенная не играет ничего.

Требования:
Anomaly 1.5.3
Modded exes: themrdemonized 20250908 или новее, либо AOEngine v0.5.2 или новее. Полный набор возможностей требует последней сборки demonized. Возможность, которой нужна более новая сборка, неактивна или работает в урезанном виде на старых exe.
xlibs (https://www.moddb.com/mods/stalker-anomaly/addons/xlibs-1001)
MCM
Anomaly Radios Extended (https://www.moddb.com/mods/stalker-anomaly/addons/anomaly-radios-extended-full-remaster-152) или похожий даёт источники радио и мегафонов
Guitar Animation от Daiviey даёт гитару, на которой играете вы (опционально)
Harmonica от Daiviey даёт гармонику (опционально)

Настройка:
Все настройки находятся на странице DiegeticControl в MCM и начинаются с собственной громкости и ритма игры.

Совместимость:
Зависит только от xlibs. Установка и удаление посреди сохранения работают. Проверено: Anomaly 1.5.3, GAMMA, EFP, Zona, Forgotten Zone.
Всё остальное сосуществует, если расширяет X-Ray и Anomaly и не перекрывает их.

Как это сделано:

Код и подходы оригинальны, построены на лучших практиках лучших модмейкеров STALKER и на обратной разработке X-Ray и скриптов Anomaly вручную.
Дизайн остаётся нативным для движка и минимальным: событийный pub/sub вместо опроса, работа распределена по кадрам через отложенные очереди и ограничители частоты, а кэши на уровень заменяют сканы мира.
Рейкастинг и математика дистанций написаны вручную и проверены под нагрузкой вживую, по стандартам и флагам X-Ray.
Где скриптинг упирается в предел движка, исправление делается в самом X-Ray, в modded exes.
Производительность - первый инвариант. Каждый поток укладывается в 2 мс, иначе сборка переписывает или отбрасывает его, профилируется постоянно с JitProfiler и проверяется вручную на неоптимизированных однопоточных exe.
Каждый мод несёт трассировку и мониторинг производительности в стиле OpenTelemetry, охватывая мировые события и каждый поток, под гейтом уровня лога, который в выключенном состоянии пропускает работу трассировки.
Каждый коммит прогоняет весь конвейер локально и в CI: luacheck, кастомную сборку selene для STALKER и тест загрузки, который запускает каждый скрипт на заглушках движка.
Слои правил затем проверяют практику Lua, истину движка, конвенции, контракты, релиз, безопасность и документацию, а гейт оценки валит сборку на любой находке в коде или безопасности.
Каждая частота, порог и переключатель вынесены в MCM или LTX, ничего не зашито в код, а любое движковое значение, которое пишет мод, остаётся в границах движка, поэтому каждое сохранение загружается.
Ему нужны только X-Ray и общий свод правил xlibs под ним, который даёт каждому моду семейства ту же защиту, дистанции, логику фракций и боевые чтения.
Он не зависит ни от одного другого мода, включая другие моды автора.
Смотрите ссылки Health и JitProfiler наверху для каждого теста и smoke-результата и для реальной стоимости CPU и памяти мода, измеренной в живой игровой сессии.

Благодарности:
Altogolik помог поддержкой, идеями и исходными материалами.

Использование и лицензия:
  Модпаки: разрешено и приветствуется. Сохраняйте файлы readme и лицензии.
  Аддоны, патчи, интеграции: разрешено. Указывайте "DiegeticControl by Damian Sirbu" заметно на странице вашего мода.
  Воспроизведение реализации в другом ПО: не разрешено, даже с указанием авторства.
  Полная лицензия в файле LICENSE и на GitHub.

Диагностика и отчёты:
Каждый релиз проходит тщательную разработку и тестирование, но баги всё равно могут проскользнуть.
Чтобы сообщить о баге, воспроизведите с включённым отладочным логированием и приложите лог мира, где у мода он есть.
Сначала исключите этот мод: воспроизведите с ним выключенным, затем включённым.
Самый чистый тест - этот мод один на ванильной Anomaly с xlibs.
Отправьте трассировки в мою ветку в Discord Anomaly: https://discord.com/channels/456765861953536020/1512539453791670402
Сначала вступите на сервер по приглашению в Discord Anomaly: https://discord.gg/c4RuJNs
Или заведите дефект на GitHub с той же информацией: https://github.com/damiansirbu-stalker/DiegeticControl/issues
Приложите xray.log, лог мода, сборку движка, модлист и порядок загрузки.
Для глубоких технических деталей и механизмов смотрите документацию по архитектуре на GitHub.

Tags: engine-native, performance, save-safe, diegetic, audio, audio-mixer, volume-control, per-source-volume, live-control, immersion, quality-of-life, reverse-engineering
