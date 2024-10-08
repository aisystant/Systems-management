---
title: Практики управления процессами и управления кейсами
---

В начале 21 века позиции проектного управления были существенно
подвинуты сторонниками процессного управления, которое главным образом
развивалось в среде «автоматизаторов» (айтишников). Увы, из этой истории
тоже ничего хорошего не получилось. Вот пример описания простейшего
«процесса» похода к доктору, который выписывает рецепт к врачу, это
выдержка из стандарта Business Process Model and Notation (BPMN)
2.0^[<https://www.omg.org/spec/BPMN/>]:


![](02-process-management-and-case-management-practices-62.png)


Такие диаграммы очень нравятся «автоматизаторам», которые пытаются
описать в проектах всё одинаковое, назвать эти проекты «процессами» и
затем это всё одинаковое автоматизировать. Особенность тут в том, что
вроде как по такой диаграмме можно попытаться рассчитать и оптимальную
загрузку каждого помянутого ресурса по типу рассуждений, которые были
для проектного управления (найти критическую ресурсную цепь, где есть
ограничение в виде Васи --- и загрузить дальше Васю как станок, удавить
мультитаскинг), но на практике это оказалось невозможным. Если у вас
одиночный простой процесс (типа «забрать деньги, выдать товар» или
«собрать вот эти три подписи на договоре»), то всё ОК. Но если речь идёт
о хоть какой-то разработке, о какой-то уникальности, то всё пропало:
сложность описания становится запредельной. А ещё ситуацию усугубляет
то, что используются для описания процессов визуальные нотации, то есть
любые изменения становятся проблемой при внешней наглядности. А в
проектах? Там по факту используется «разбиение работ» (аутлайн,
«дерево») и много более простые диаграммы
Гантта^[[https://ru.wikipedia.org/wiki/Диаграмма\_Ганта](https://ru.wikipedia.org/wiki/Диаграмма_Ганта)].

Итого: **управление процессами для целей операционного менеджмента «не
пошло»**, оно помогало айтишникам что-то автоматизировать, но для работы
с людьми по части управления порядком загрузки ресурсов (а мы только что
убедились, что этот порядок важен для минимизации сроков выполнения
проектов, «чистая арифметика» важна) оказывалось не очень пригодно. **По
факту «процесс» стало синонимом слову «практика» (труд, деятельность), а
«работа»** **по этой практике ---** **это «экземпляр процесса».** С
экземплярами процесса предмет (дисциплина из учебников) процессного
управления не работал, отсылая к предметам дисциплин теории массового
обслуживания/теории очередей и исследования операций. Но для «процесса
заключения договора» в софте процессного управления всегда можно было
найти, что происходит с каждым конкретным договором. **Учебники
управления (организационными) процессами/business-process**
**management** **не рассказывали про то, что и как делать с
«экземплярами»,** **но софт** **работу с экземплярами поддерживал.** Так
что **«управление процессами» по факту оказалось инженерной** **(про
содержание работ, про практики), а не менеджерской** **(про логистику,
про работы)** **практикой.**

Засилье процессного подхода кончилось в одночасье:

-   Всё процессное автоматизируется и перестаёт называться «процессом»
    (и даже «автоматизацией»: при автоматизации часто меняется суть
    работы, одна практика заменяется совсем другой, управлять нужно уже
    совсем другим набором работ)
-   «Процессом» называют всё что ни попадя, но кроме названия там уже
    мало что остаётся от классической
    пошаговости^[<http://ailev.livejournal.com/1195297.html>].
    Это только кажется, что у людей в головах именно «процессы». В
    головах у них «практики», BoK вместо «пошаговых расписаний».
    Процессом также часто называют и вид жизненного цикла в целом (agile
    process, engineering process).
-   Упор на рабочие продукты (case management, issue tracking),
    облегчает договорённости --- это отсылка к 4D, об этом мы расскажем
    чуть подробней ниже.
-   Практики мы описываем не как огромные методологии, в которых чётко
    прописаны длинные сценарии, а как отдельные короткие элементы
    практик, из которых можно по обстоятельствам собирать длинные
    цепочки --- гранулярность обеспечивает ситуационная инженерия
    методов, которая рассказывает нам, из каких элементов состоят
    практики (всё это крутится вокруг альф, изменения состояния альф и
    т.д.). Акцент поэтому оказался не на собственно «процессах» как
    длинных цепочках (иногда это «маршруты» и обсуждается
    **маршрутизация/routing**, иногда это обсуждается как «сценарии»,
    иногда как **поток работ/workflow**, то есть работы, идущие/flow
    через людей и компьютеры), а на инструментарии описания коротеньких
    процессов из их элементарных частей.
-   Декларативность (правила пред- и постусловий, а не указание
    последовательности), то есть длинные описания сценариев не
    существуют. Просто из какой-то библиотеки элементов кейсов
    последовательность работ собирается путём подбора нужных по
    предусловиям. Появился OMG CMMN (Case Management Model and
    Notation)^[<https://www.omg.org/spec/CMMN>]
    в дополнение к процедурному BPMN 2.0 как поддерживающий это язык, но
    он не получил распространения, декларативное программирование очень
    удобно для разных описаний, но очень тяжело в понимании (в
    классическом программировании «все хотят писать
    декларативно^[[https://ru.wikipedia.org/wiki/Декларативное\_программирование](https://ru.wikipedia.org/wiki/Декларативное_программирование)] ---
    функционально или на логическом языке, но получается всё равно
    императивно» --- с составлением длинных цепочек работ то же самое,
    «все хотят описывать их функционально или логически, но получается
    императивно», в процессном управлении приняты императивные описания
    «шагов программы/шагов работ»). Так же не получил большого
    распространения механизм декларативного описания организационных
    норм/business
    rules^[<https://ailev.livejournal.com/693597.html>],
    не стали популярными реализующие его стандарты OMG
    SBVR^[<https://www.omg.org/spec/SBVR/>]
    и привязанный к стандартам описания процессов OMG CMMN
    (декларативный) и OMG BPMN (императивный) стандарт описания принятия
    решений в ходе выполнения работ OMG
    DMN^[<https://www.omg.org/spec/DMN>].

А что там с практиками в проектном управлении, как там работают с
«одинаковым» в предметной области? Там ровно наоборот: всё про работы и
их уникальную логистику в части «экземпляров» применения практик, и
намеренный уход от любого обсуждения «типовых работ» (хотя понятие
«процесс» как практика используется, начиная со второго поколения --- но
только для процессов проектного управления, а не для процессов самого
проекта, ибо «какие такие процессы? У нас всё уникально, у нас
экземпляры!». В процессном управлении невозможно поставить даты
выполнения работ, а проектном управлении невозможно завести работу без
даты. Но поскольку практики и связанные с ними работы таки существуют,
софт (но не учебники!) проектного управления поддерживает «шаблоны
проектов». И даже если простейший софт (например, MS Project) не
поддерживает, то мало кто начинает работу над планированием нового
проекта с пустого разбиения работ. По нормам проектного управления
разбиение работ обязано содержать даты начала каждой работы и ресурсы на
её выполнение, поэтому невозможно иметь разбиение работ без привязки ко
времени (такое описание будет, скорее, описанием практики, «описание
процесса::практика работы::работа»), но в жизни просто берут предыдущее
описание проекта с проставленными датами начала и конца работ, и
чуть-чуть редактируют состав работ (или даже не редактируют), а вместо
старых дат ставят новые. Так что «шаблона проекта» вроде бы нет (каждый
проект уникален!), но по факту он есть.

И помним, что были ещё программы проектов, где вроде как признавалось,
что могут появляться по ходу выполнения проектов какие-то новые идеи о
новых продуктах/фичах, и это порождает новые проекты. То есть состав
работ уже представлялся не таким постоянным, допускалось планирование
«на лету». Хотя это и не называлось «перепланированием уже идущего
проекта», но на деле отличия программы и проекта были не такие уж и
большие. Проектные офисы (которые должны были помогать управляющим
проекта вести проекты по новой практике проектного управления) вдруг
обнаружили себя в ситуации, в которой никому помогать уже не надо, все
уже знают про управление проектами и получили сертификаты проектных
управляющих, практика оказалась уже не новой, а старой. **Поэтому
проектные офисы** **стремительно переквалифицировались в программные
офисы** --- начали помогать вести программы проектов и увязывать между
собой ресурсы всей производственной программы с текущими проектами, а уж
с отдельными проектами разбирались люди сами, все уже были обучены.

В ответ на все эти сложности и в проектном, и в процессном управлении
родился ещё один подход, который по факту стал центральным/mainstream
(пару раз поменяв при этом название): **управление кейсами/ведение
дел/case** **management**. Сам этот подход появился из лечебных дел/case
и судебных дел/case и тесно связан в его понимании как «папки Дело
№\_\_\_» или «папки истории болезни» (папка дела/case file).

Внимание для всех практик и работ в управлении кейсами удерживалось тем,
что какой-то объект (предмет дела/кейса), который нужно было перевести
из начального в конечное состояние становился точкой сборки. Это как
vision в стратегировании определяет разные варианты mission и допускает
разные работы по его получению, это как программа проектов должна
достичь целей программы, а уж проекты в её составе могут быть самыми
разными для достижения целей. Тем самым постулировалось, что «прибыть из
точки А в точку Б можно огромным числом способов, работы могут быть
разными, а вот закончиться они должны одинаково: прибытием в точку Б».
При этом цель задавалась как vision (состояние мира), но сам кейс был
mission, и тип кейса --- даже не «практика», а «работа» (кейсы
уникальны, если не уникальны, то это «шаблоны»). Запомнили:
кейс::работа, «шаблон кейса»::практика.

Основной режим планирования в управлении кейсами --- когда ты не знаешь
заранее/upfront, что делать, поэтому планируешь работы «в связи с
открывающимися обстоятельствами дела/case», как в судебных делах --- с
каждой новой найденной уликой или доказанным алиби планы следствия и
суда меняются. Так же и в больнице, каждый новый анализ может открыть
что-то такое, что полностью поменяет диагноз и направление лечения. С
одной стороны, когда больной поступает в больницу, невозможно
представить его прохождение по кабинетам в виде связного «процесса
лечения», ибо там будет всё дико запутано --- сто кабинетов со ста
видами анализа и диагностики и ещё сто кабинетов со ста видами процедур
лечения. С другой стороны, цель понятна: пациент здоров и выписывается.
То есть каждый кабинет вроде как процессный (всё там одинаково --- укол
ставят и анализ крови делают «на потоке», всем более-менее по одной
процедуре), а вот последовательность прохода по кабинетам разная для
каждого кейса (где больной пациент --- предмет кейса: его надо перевести
в состояние «здоровый человек, не пациент»). И планирование идёт на
каждом шаге.

Так что в управлении кейсами не столько «составление плана и
отслеживание выполнения плана» как в управлении проектами, сколько
«принятие решений по следующим работам и отслеживание выполнения
решений». В бизнесе сюда более-менее укладываются практики выполнения
поручений, практики исправления ошибок --- все те практики, где на вход
поступают явные «кейсы», которые надо как-то учесть и отследить, чтобы
все эти работы были выполнены. Затем было осознано, что **все практики,
где есть выдвижение гипотез (вся разработка, вся архитектурная
работа) ---** **это ровно такие практики,** **которые нельзя
запланировать заранее. А заранее планировать можно только производство и
сборку. Поэтому управление кейсами в разработке является основной
практикой управления работами.**

Софт для такого отслеживания/tracking называется трекерами. Каждый кейс
может быть назван проблемой/issue, поэтому софт этот --- issue trackers
(bug tracker, incident tracker и т.д.). Главное, что в трекере up front
планирование вроде как не поддерживается отсутствует (непонятно, когда
что будет делаться), но зато поддерживается up front «шаблонирование», в
том числе если понятна грубо цепочка/маршрут, по которому должны будут
пройти работы какого-то типа (работы по какой-то практике), то это можно
заранее тоже записать в шаблоне. Но можно и без шаблона --- записать
просто для учёта/отслеживания. Помним, что очередной кандидат на пятое
обязательное описание --- это WBS, work breakdown structure (по факту
это описание работ создателя). Это вот то же самое: попытка описать
конфигурацию текущих работ, отследить возможный «развал конфигурации»
(работы не имеют предмета работ, работы идут с игнорированием SoTA
практики работ, работы идут по пять штук одинаковых над одним предметом
работ, все ресурсы/исполнители назначены не на самые нужные работы и
т.д.), но в case management разрешается планирование работы делать прямо
перед её выполнением.

Тем самым issue trackers работ обычно идут в связке с репозиторием
версий предмета кейсов (помним, что у каждой работы есть её основной
предмет), но issues появляются там или up front (например, я заранее
знаю, что ошибки будут, и делаю шаблон работ по исправлению ошибки, то
есть прописываю практику, по которой будет порождена работа в момент
появления экземпляра ошибки), или вот прямо после понимания, что
какая-то работа должна быть сделана в ситуации, которую никто не
предполагал (кейс «убрать царапину неизвестного происхождения, которая
появилась на корпусе прибора вчера ночью»). Кейс таким образом проходит
самые разные состояния, например: issue («непонятно, что делать и с чем,
но vision есть --- чтобы на корпусе не было царапины»), далее это
становится task::«работа из проектного управления, которая понятно по
какой практике делается, и понятно когда и кем» (mission --- закрасить
царапину и заполировать, делает Женя как самое срочное дело), но затем
ещё и обязательно notice (мир изменился, и всех заинтересованных в его
изменении надо оповестить об этом --- этот шаг нельзя пропускать).

Итак, к программам проектного управления (диаграмма Гантта на экране и
часами идущее «планирование» перед «выполнением плана работ») добавились
программы процессного управления (заполнение формочек параметров
экземпляра процесса по заранее подготовленным моделям процессов, если
речь идёт о людях, но это может быть и полностью автоматизировано ---
тогда ничего заполнять не надо, но «процесс идёт хорошо, экземпляры
процесса порождаются автоматически»), добавилось управление кейсами, где
и практики (шаблоны кейсов) и работы (сами кейсы), и возможно upfront
планирование, и возможно планирование работ, ведущихся «открывающимися
обстоятельствами дела» и дальше не столько планирование и отслеживание
выполнения плана, сколько отслеживание/tracking хода работ (ибо плана-то
нет, разве что «шаблоны», где они осознанны и документированы).

Управление программами тем самым --- это такое управление кейсами, где
работа-проект планируется непосредственно перед её выполнением, но для
неё не говорится о практике (шаблоне), ибо вроде как для проектов не
должно быть какой-то повторяемости. Управление кейсами оказалось
всеохватным, при этом чтобы как-то отстроиться от чисто медицинских
«историй болезни» и судебных «дел», это всеохватное управление кейсами
начало себя называть как **динамическое/dynamic** **управление кейсами,
адаптивное/adaptive** **управление кейсами** (самое популярное), были и
другие модификаторы названия.

В реальности в каждом большом проекте можно встретить какие-то его
части, которые были сделаны согласно требованиям какой-то из школ
управления. Хорошим примером тут был случай зимней олимпиады 2014 года в
Сочи, где в управлении было примерно 5000 кейсов от строительства
(внутри эти кейсы велись программами проектного управления), примерно
5000 кейсов пришли от системы управления качеством собственно Олимпиады
(выполнение требований Олимпийского комитета) и ещё примерно 5000 кейсов
пришли в качестве поручений от первых-вторых лиц государства. Тем самым
под управление российской командой организации олимпиады попало примерно
15 тысяч
кейсов^[<https://ailev.livejournal.com/1176241.html>].
Поскольку в самом начале работ было непонятно, что это за такой странный
объект у них в управлении (кейс-менеджмент не рассматривался, ибо на
слуху у всех было «проект» и люди хотели получать премии за выполнение
проектов), то примерно 35 человек из Microsoft написали специальный софт
для сопровождения этого винегрета «проектов на контроле». Терминология
использовалась проектного управления, но перед самым стартом Олимпиады
люди сообразили, что это кейс-менеджмент! И появилась идея по-быстрому
перегрузить все 15 тысяч кейсов в простую программу issue tracker
(предлагался open source
Redmine^[<https://www.redmine.org/>], тем
более что он позиционировался не как issue tracker, а как «flexible
project management web application»). Этого не случилось, поскольку эти
идеи появились буквально за три недели до старта Олимпиады, и просто
испугались каких-то потерь данных при переливе информации по 15 тысячам
кейсов плюс какому-то переучиванию людей команды. Решили, что
«продержимся ещё три недели, потом Олимпиада --- и всё, конец истории».
Но если бы люди понимали суть управления кейсами, то жизнь их была бы
проще!

Управление кейсами потребовало не только отдельной идеологии, но и
отдельных программ (простые issue trackers явно не учитывали
полноценного варианта case management в части адаптивности, которая
понималась как «шаблоны готовят непрограммисты») --- а поскольку
выяснилось, что эти программы решают огромное количество проблем, то они
были выпущены и стоили баснословные деньги. Это всё случилось как раз в
2013-2015 году, и потом идеи адаптивного управления кейсами исчезли под
этим названием, но не исчезли из жизни:

-   Большинство issue trackers были переименованы в «программы
    управления проектами», хотя помним, что они появились сначала по
    линии процессного управления, ибо «шаблоны кейсов» были по факту
    описанием практик! Но процессное управление «про практики», а
    работами-проектами надо было управлять, поэтому победило слово
    «проектное управление», но оно оказалось не тем, что в классическом
    проектном управлении, совсем другое body of knowledge! С другой
    стороны, чтобы быть более похожими на программы проектного
    управления кейсы могли быть представлены на верхнем уровне в
    современных программах в виде диаграмм Гантта!
-   Появились универсальные табличные моделеры (notion.so, coda.io и
    прочие), которые хорошо подходили под идеи LowCode и NoCode. Это
    LowCode формулировалось как «непрограммисты могут написать какие-то
    простейшие процессы/workflow», то есть код, поддерживающий
    отслеживание/tracking работ по какому-то шаблону. Но это как раз
    совпадало с тем, о чём говорилось в adaptive case management.
    Дорогие специализированные программы управления кейсами массово
    начали отпадать, и прототипирование работы с шаблонами кейсов
    массово перешло в это универсальное моделирование. Но если кейсы по
    каким-то шаблонам оказывались реально массовыми, или оказывались
    кейсами не изменений в реальном виде, а кейсами обработки
    информации, то это просто переносилось в специализированный
    «процессный софт».

Итак, у нас есть несколько разных методов управления работами:
управление проектами (классическое), управление программами, управление
процессами, управление кейсами. Как определить, для Васи, исполняющего
какую-то практику MX (например, приготовления кофе с молоком с
использованием кофе-машины для Клавдии, практика эта разбиралась в курсе
«Методология») --- это программа, проект, процесс или кейс?! Мы довольно
быстро договоримся, что результатом там должна быть чашка капучино в
состоянии «сервировано у Клавдии» (ибо надо будет учесть и особенности
подачи --- все эти блюдца, салфеточки, опциональный сахар и ложечку). Но
ведь тренированный специалист и напишет, и обоснует это всё как проект
(в PRINCE2 как раз в названиях работ и проектов рекомендуют писать их
результат, это близко к кейсам, где кейс тоже называют по предметам
кейса). Примерно так же можно обосновать, что это процесс, и что это
кейс! Напомним, что основные критерии там --- это «работа будет
повторяться по шаблону много раз» или «нет, работа уникальная
одноразовая, никакого шаблона». Но дальше в софте обязательно
оказывается, что поддерживается и одно, и другое (понятно, что нужно и
практику поддержать, и экземпляры задействования практики --- работы).
Вот тут «что только в софте» показано пунктиром, а что «в учебнике
дисциплины» показано сплошным контуром:


![](02-process-management-and-case-management-practices-63.png)


Тут важно, что вопрос из предыдущего абзаца задан некорректно. Для этого
вернёмся к 4D представлению мира:

-   Вот Вася готовит капучино для Клавдии в реальном мире, прямо в
    физическом мире, в 4D (то есть он, кофе, молоко, кофе-машина, чашка
    и т.д. занимают пространство-время), он работает.
-   А вот Илья, имеющий знания по проектному управлению, описывает это
    как проект (каждая чашка кофе уникальна, каждый посетитель требует
    что-то своё! Это неважно, что эти проекты похожи: в учебниках этого
    нет, но просто задействуем софт проектного управления достаточно
    мощный, чтобы в нём был «шаблон проекта». При этом помним, что в
    проектах есть подпроекты, а проекты получаются из программ. Так что
    берём программу «сделать Клавдию довольной», порождаем проект
    «напоить капучино», там внутри, конечно, подпроекты приготовления
    кофе, капучинирования, подачи. Можно хорошо описывать разделение
    труда, привлечь Петю для капучинирования!). Получается, что работа
    сама происходит в 4D уж как происходит, но она **описана** как
    проект! Проектное управление в его классическом варианте --- это
    метод описания, viewpoint, а описание --- это всего лишь view на
    работу, а не сама работа! **Правильно говорить не «работа Васи ---**
    **это проект», а «работа Васи описана/классифицирована как
    проект»!**
-   То же рассуждение для Ольги, имеющей знания по процессному
    управлению, она описывает это как процесс. Не будем расписывать
    подробно. Работа в физическом мире, но она будет описана как
    процесс, это только одно из возможных описаний.
-   И Крис, который только-только узнал об управлении кейсами, он опишет
    эту работу Васи как кейс --- но это никак не помешает существовать
    описаниям Ильи этой работы как проекта (и даже программы работ!), и
    описанию Ольги как процесса, и описанию Криса как кейса.


![](02-process-management-and-case-management-practices-64.png)


Нет «на самом деле» проектов, процессов, кейсов! Это всё разные акценты
моделирования одной и той же реальности живой работы (а хоть и будущей,
у нас 4D).

Получается, что правильный вопрос --- это не «что такое работа Васи на
самом деле», а «как нам удобно описывать эту работу». И тут нужно
предупредить, что «удобно» --- это не «как я привык», ибо метод описания
не должен выбираться по поговорке «когда у ребёнка в руках оказывается
молоток, то все предметы в доме превращаются в гвозди» (если я закончил
курсы проектного управления, то все работы будут у меня проектами, а
процессы тоже будут --- «открытия проекта», «ведение проекта» и так
далее, всё с проектами):


![](02-process-management-and-case-management-practices-65.png)


Каждый вариант нарезки мира работ по факту ведёт к выбору софта, который
хорошо поддерживает ответы на какие-то определённые вопросы:

-   Проектное управление (графики работ и задействования ресурсов ---
    отвечает на вопрос «когда кто что должен делать»? И помним, что без
    нормирования работ, учёта ресурсов, возможности знать все работы до
    начала проекта --- не работает, ответа на вопрос не будет!)
-   Теория массового обслуживания (потоки и очереди --- переварим всё
    однородное за минимальное время! Сколько надо иметь ресурсов, чтобы
    мы справились? Но нет ответов на вопрос «когда и кто будет делать»,
    это всё «в рабочем порядке»)
-   Процессный подход в смысле BPMN (кто что должен делать, но вот
    когда --- непонятно, «когда работа будет готова»)
-   Адаптивное ведение дел/case management/«отслеживание/tracking
    проблем/issue, багов/bugs, происшествий/incident» и дальше разные
    варианты Workflow с LowCode и даже NoCode (тут обычно
    agile/шустрость в реакции на непредсказуемое: удерживать во внимании
    цель, чтобы её достичь, но по какому маршруту пойдут работы, и какие
    они будут, заранее неведомо. Но мы удержим внимание!)
-   Потоки пользы / value
    networks^[<https://en.wikipedia.org/wiki/Value_network>]
    (бизнес, т.е. кому это выгодно). Мы не поминали это, но в некоторых
    организационных практиках такое описание работ тоже может
    использоваться --- чтобы обнаруживать работы, которые не приносят
    никакой пользы. В этих сетях указывают оргроли, и кто кому что
    предоставляет (deliverables) --- чтобы на выходе получить итоговую
    систему, дающую пользу. Но легко представить, что речь идёт о
    работах, которые надо выполнить, чтобы получить эти deliverables.

Так что мы рекомендуем:

-   Где можно, используйте кейс-менеджмент, ибо там наиболее общее
    описание работ. Объявляйте альфы как объекты внимания в проекте
    кейсами, описывайте их состояния, формулируйте для этого контрольные
    вопросы, добивайтесь ответов на контрольные вопросы путём выполнения
    работ, которые ведутся по каким-то практикам. Всё это моделирование
    записывайте в табличном формате, или используйте какой-то подходящий
    софт (например, PLM-систему, если речь идёт о машиностроении или
    стройке).
-   Смело смешивайте любые описания, если вам нужны какие-то ответы на
    вопросы, или решение каких-то проблем. Например, смело называйте
    кейс проектом, или даже программой. И задействуйте issue trackers,
    которые сейчас тоже называются софтом управления проектами (хотя
    этот софт совсем не похож на софт классического управления
    проектами). На верхней паре уровней декомпозиции кейсов на подкейсы
    огромного проекта говорите «директивный график» и переходите на язык
    классического управления проектами (ибо там будут «директивные
    сроки», которые даже не прогнозные, а предписанные по интуитивным
    оценкам дедлайны, конкретные даты). Вас поймут все менеджеры. А ниже
    переходите на язык разговора о кейсах и отслеживания/tracking
    проблем/issues, только часть из которых известна upfront/перед
    началом работ --- и вас будут понимать все разработчики, архитекторы
    и инженеры платформы/DevOps/internal development platform engineers.
    Общий принцип: с менеджерами старой закалки говорите на языке
    классического управления, это будет ласкать им слух (даже в случае
    работ по разработке, к чему категорически проектное управление
    противопоказано), а с инженерами «от сохи» говорите на языке
    управления кейсами.
-   На забывайте, что основных альф у нас много --- на каждое звено
    цепочки создания по нескольку, и нужно ещё добавлять подальфы, ибо
    основных альф обычно не хватает для разбирательства с состоянием
    проекта. То есть работы должны быть и непосредственно меняющие
    состояния альфы «воплощение системы», и альфы описания системы, и
    альфы описания работ системы, и для нужных вам альф в зоне интересов
    к надсистеме --- и это для каждой системы в цепочке создания.
-   Все неожиданности (включая обнаружение и исправление ошибок, а также
    выдача поручений начальством «из ниоткуда») должны рассматриваться
    как кейсы, иначе запутаетесь.
