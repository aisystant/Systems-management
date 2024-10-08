---
title: Практика управления проектами
---

Управление работами (операционный менеджмент, логистическое
рассмотрение) противопоставляется управлению жизненным циклом как
разбирательству с практиками --- и подробно разбиралось в курсе
«Методология». Там, в частности, было рассказано, что управление
жизненным циклом сначала было неотличимо от «грубого управления
работами» (где «грубого» --- это деление на несколько больших стадий,
или этапов, понимаемых как одноуровнево представленные работы системы
создания, но обычно не мельче), а дальше появилось управление жизненным
циклом 2.0, в котором на первый план вышли практики в их неразрывной
связи с работами, которые реализовывали эти практики. И там же
рассказывалась история появления в системном движении не только
системной инженерии, но и управления проектами. Но дальше «Методология»
сосредотачивалась на раскрытии понятия практики, а что происходит в
проекте с работами, не обсуждалось. Это и есть водораздел: в управлении
жизненным циклом рассматриваются подробно на много уровней декомпозиции
практики, но вот работы --- только самого верхнего уровня
(фазы/стадии --- и то в условиях «непрерывного всего» это уже
сомнительное рассмотрение работ), а в управлении работами/операционном
менеджменте практики рассматриваются главным образом самого управления
работами/операционного менеджмента, а работы дробятся на достаточное
число уровней.

Сам **проект** создания и иногда даже развития системы (то, что делают
создатели в их цепочках) рассматривался как единица применения практики
инженерии (практики создания и развития систем) и он же --- как большая
работа, ведущаяся по этим практикам. При этом в жизни слово «проект»
чаще всего ассоциировалось как раз не с практикой инженерии (и далее
обсуждением способов ведения инженерных работ), но с набором работ (и
реже --- было синонимом оргзвена, ведущего работы, то есть «проект» был
вроде как «оргзвено, ведущее работы», а не «поведение оргзвена, то есть
сами работы»).

И системная инженерия, и управление проектами во втором поколении
системного мышления исходили из гипотезы тщательного upfront (то есть
перед изготовлением) проектирования системы и проектирования работ
(проектирование работ --- это планирование). В 21 веке это
«предварительное планирование» стало встречаться очень редко, ибо работы
превратились из однократного проектирования системы и изготовления
системы, удовлетворяющей требованиям (водопад) в «непрерывное всё»,
которое подпитывается непрерывными изменениями в окружении целевой, во
всё более известном поведении самой целевой системы, в устройстве
цепочки создания и доступных этой цепочке практик работы с их
обновляющимися технологиями, в выдвигаемых всё новых и новых гипотезах о
новых и новых потребных фичах целевой системы. Слово «проект» осталось,
но перестало обозначать обязательное предварительное планирование и
какое-то внятное окончание работ по выполнению обязательств: начало
проекта примерно понятно, а вот конец уже непонятен (создатель начинает
делать систему, и развивает её «пока смерть не разлучит нас»).

Само **проектное управление в его классическом виде** **всех поколений
исходит из трёх посылок, и если их нет, то его попросту нельзя
использовать, потому как не будет работать,** практики окажутся
неприменимы:

-   **Есть нормы** **производительности труда,** то есть можно как-то
    планировать продолжительность работ (скажем, в строительстве
    кирпичных домов для кирпича есть норма, сколько каменщик укладывает
    кирпичей в час --- и на эту оценку можно как-то опираться).
-   **Есть учёт ресурсов** (то есть можно сказать, сколько строительный
    рабочий работал, выполняя какую именно работу: сколько каменщик
    укладывал кирпичей, сколько замешивал раствор, если вдруг он
    оказался ещё и на этой операции).
-   **Заранее известна последовательность работ (up** **front**
    **plan),** в том числе это означает, что заранее известен состав
    системы (ибо план получают из того, что для каждой части системы
    планируют работы по её проектированию, изготовлению, логистике к
    месту сборки/монтажа, сборке/монтажу, испытаниям).

Если внимательно приглядеться, то это всё будет работать или на
заводском машиностроительном **производстве/manufacturing** под заказ
(без работы конструкторского бюро! Только производство!), или на стройке
на стадии именно «строительство» (но не стадии проектирования). Везде,
где есть хоть какие-то неопределённости (скажем, в умственной работе не
установишь норму на решение проблем, типа «полторы проблемы в сутки»,
или в условиях выдвижения и критики гипотез не скажешь заранее
последовательность их выдвижения и критики, включая экспериментальные
проверки, то есть нет «плана работ по изобретению системы»),
классическое проектное управление не работает.

Само это классическое проектное управление прошло несколько поколений,
сейчас мы наблюдаем четвёртое (которое по большому счёту уже не очень
классическое именно «проектное управление», смысл понятия поменялся):


![](01-project-management-practice-60.png)


Первое поколение говорило только то, что есть отдельные работы, которые
хитро связаны друг с другом (представляются какой-то сетью/network), и
их нужно как-то выполнить ограниченным ресурсом за минимальное время ---
представить график. Метод получил русскоязычное название «сетевое
планирование» (основной объект там --- «сетевой
график»^[[https://ru.wikipedia.org/wiki/Сетевой\_график](https://ru.wikipedia.org/wiki/Сетевой_график)],
отражающий зависимость работ друг от друга), по-английски получил
распространение как Program (Project) Evaluation and Review Technique,
или
PERT^[<https://ru.wikipedia.org/wiki/PERT>].
Суть этой техники в том, что находился критический путь/critical path
как собранная от начала работ до конца проекта самая длинная цепочка
работ, которые нельзя начинать раньше, чем закончится предыдущая работа
по цепочке. Если сократить длительность работ в этой цепочке (скажем, не
допускать пауз при переходе от одной работы в цепочке к другой работе),
это автоматически уменьшало время работ по проекту, или хотя бы давало
какую-то предсказуемость времени ожидаемого окончания работ.

Второе поколение родилось, когда появилось понятие процесса как
повторяемого паттерна работ (по факту речь шла о практиках). Процесс
считался реализацией какой-то практики, и всё стали изображать как
базовые единицы-процессы. Процессы рассматривались как
commodities^[<https://en.wikipedia.org/wiki/Commodity>]
(базовые товары на товарно-сырьевой бирже, типа зерна или нефти:
качественные различия мало волнуют, поставщики мало волнуют, одна партия
легко заменяется другой партией). Проект же во втором поколении
рассматривался как нечто уникальное, составленное из более-менее похожих
процессов. Скажем, процессы «открытие проекта», «планирование работ»,
«ведение работ» не уникальны (они определяются практикой проектного
управления, которая будет одинакова, где бы она ни применялась --- хоть
в проектах выращивания арбузов, хоть в проектах производства кремниевых
микросхем). Но вот сами работы, которые по ним ведутся, в совокупности
уникальные --- это и будет «проект». Появилось множество самых разных
практик второго поколения управления проектами как отдельной дисциплины:
Project Management body of Knowledge
(PMBoK)^[<https://www.pmi.org/pmbok-guide-standards/foundational/pmbok>]
от PMI (Project Management Institute), PRojects IN Controlled
Environments
(PRINCE2)^[<https://en.wikipedia.org/wiki/PRINCE2>]
и многие другие.

Проблем с этим вторым поколением было две:

-   Обнаружилось, что «управлять проектами» нужно главным образом путём
    переброски временно свободных (находящихся не на критическом пути)
    ресурсов одного проекта на работы критического пути (критического
    ресурсного пути пока не рассматривали, это появится позже) другого
    проекта. Это заставляло задумываться не столько о проекте, сколько о
    его окружении и называлось «достижение глобального максимума» (то
    есть нельзя было минимизировать время прохождения одного проекта за
    счёт ухудшения времени прохождения всех остальных проектов, а каждый
    проект пытался оттянуть ресурсы на себя, в методологиях проектного
    управления чётко говорилось, как управляющим проектам это нужно
    обосновывать и как этого добиваться --- впрочем, если вам поставят
    бонус в зарплате за досрочное выполнение проекта, то вы будете
    заинтересованы в получении своего бонуса, а бонусы других
    управляющих вас будут волновать мало. В итоге война всех со всеми,
    ибо проекты никогда не идут по одиночке).
-   Запланировать заранее работы вообще невозможно, ибо в жизнь
    врывается «непрерывное всё». В жизни это называлось agile. То есть
    ты вроде как должен планировать, но в первый момент проекта
    абсолютно непонятно, что же именно планировать, а за изменение
    планов тебя бьют --- но оно же неминуемо! Поэтому жизнь происходила
    одним образом, а отчётность по проектам была абсолютно другой,
    «глянцевой». Планы составлялись бессодержательные, типа «первый
    этап», «второй этап», «третий этап», а что там за работы в них были
    и почему они столько стоят и столько длятся --- это обсуждать было
    невозможно.

Ответом было появление систем проектного управления третьего поколения,
где «проект» оказывался более-менее элементарной работой (хотя и сложно
устроенной), а на передний план выходило понятие **программы**
**проектов**^[[https://ru.wikipedia.org/wiki/Программа\_проектов](https://ru.wikipedia.org/wiki/Программа_проектов)]
как совокупности всех проектов, возможно ещё не начатых. Можно долго
обсуждать, чем **портфель проектов** как совокупность всех проектов
отличается от
программы^[[https://ru.wikipedia.org/wiki/Портфель\_проектов](https://ru.wikipedia.org/wiki/Портфель_проектов)],
но понятие портфеля проектов попросту отсылает к отдельным проектам,
лежащим в портфеле (оно вполне присутствовало и в первом поколении
проектного управления). А вот программа работ особо напирала на то, что
очередные проекты в программе появляются по мере осознания в них
необходимости, а уже появившиеся проекты пересекаются по ресурсам,
параллельны по времени, а также все могут быть оптимизированы под
понятный результат программы. И, конечно, все эти рассуждения сильно
затуманивались тем, что во втором поколении проектного управления
менеджмент весь в целом и менеджмент проекта по факту отождествлялись:
если взять руководителя проекта и директора фирмы, то сразу и не
поймёшь, чем они различаются --- оба должны вроде как быть лидерами,
организовать вверенные им коллективы, вести переговоры с контрагентами,
следить за финансами и т.д. Суть «управления работами» оказалась
существенно размыта в общеменеджерских рассуждениях.

В третьем поколении классического проектного подхода была сделана
попытка преодоления замеченных проблем. Основным объектом проектного
управления стал не проект, а **программа проектов** **(производственная
программа, программа развития и т.д.)**, частями которой стали проекты.
Управление проектами (уже объявленными) осуществлялось в рамках
перераспределения ресурсов во всём текущем **портфеле проектов** (то
есть уже известных проектов), но смысл «программности» был в том, что по
мере осознания того, что нужно делать для достижения целей программы,
формулировались и запускались новые проекты программами. Это получило
название **управления программами**, в котором с одной стороны нужно
вовремя запускать новые проекты::работы, чтобы двигаться к объявленным
целям программы (выполнять миссию достижения видения, где отдельные шаги
ещё не известны и будут определяться по мере продвижения в выполнении
миссии), а с другой стороны, как можно быстрее выполнять на ограниченном
множестве ресурсов те проекты::работы, которые уже известны на данный
момент. Так сказать, оптимизировать известное, пытаясь оптимизировать
ещё и неизвестное. К этому классу методик проектного управления третьего
поколения относились популярное в Японии Program and Project Management
(P2M)^[<https://www.pmaj.or.jp/ENG/p2m/p2m_guide/p2m_guide.html>],
проектное управление из теории ограничений
(TOC)^[<https://asana.com/resources/theory-of-constraints>].

Основное, что было выявлено в ходе всех этих попыток сформулировать
проектное управление:

Важнейшим является управление потоками работ через какие-то рабочие
станции. Ресурсами тут будут сырьё и промежуточные материалы, но и сами
рабочие станции. Задача проектного управляющего в том, чтобы убирать
ограничения в производительности. Логисты (в supply chain), проектные
управляющие --- это всё одно и то же в части моделирования
происходящего, ключевой объект --- **поток/flow, который течёт по сети
рабочих станций/ресурсов**.

Рассматривать приходится сразу все потоки работ, ибо оптимизировать один
поток работ (проект) так, чтобы не ухудшить при этом протекание всех
потоков работ (производственную программу) невозможно. «Оптимизировать»
тут сводится к выполнению чисто арифметической задачи: какие работы в
какой последовательности поручать выполнять рабочим станциям.
**Арифметика решает всё, и она контринтуитивна.** В каждой
производственной сети есть ограничение на общее время выполнения работ,
и оно зависит не только от последовательности работ (первое и второе
поколение проектного подхода --- в них упор делался на метод
**критического пути/critical** **path**), но и от наличия ресурсов,
которые доступны (метод **критического ресурсного пути/critical**
**resource** **path/критической цепи/critical** **chain**). В случае,
когда для многих проектов у нас одни и те же ресурсы (множество проектов
идёт через одних и тех же людей), практически бесполезно стало говорить
о критических путях --- ибо всё уже решали не длительности работ, а
доступность ресурсов, которые разрывались по разным проектам.

**Самое контринтуитивное тут ---** **это понять, что арифметика решает
всё.** **Без рационального понимания того, что порядок выполнения работ
на множестве ресурсов крайне важен, невозможно управлять проектами.**

Предположим, у нас есть три заказа, каждый из которых требует выполнения
трёх операций. Беда в том, что у нас есть только один работник Вася,
который может выполнять операцию MX, а остальные операции могут
выполнять самые разные другие люди.


![](01-project-management-practice-61.png)


Если бы было три Васи, то все работы закончились бы на тридцатый день.
Но Вася один. У нас есть самые разные варианты того, как загрузить Васю
работой.

Первый вариант «бесчеловечный», основан на чистой арифметике: Васе
говорим, что он не имеет права заниматься ничем другим, пока не сделает
работу MX для одного проекта, потом для другого, потом для третьего.
Относимся к Васе как к станку! Дальше никаких чудес: первый клиент
получает результаты через тридцать дней, второй через сорок, третий
через пятьдесят дней. Это обсуждается обычно в **управлении процессами,
и там в основе теория массового обслуживания/теория
очередей**^[[https://ru.wikipedia.org/wiki/Теория\_массового\_обслуживания](https://ru.wikipedia.org/wiki/Теория_массового_обслуживания)]
**и исследование
операций**^[[https://ru.wikipedia.org/wiki/Исследование\_операций](https://ru.wikipedia.org/wiki/Исследование_операций)]**.**
Упор на то, что работа MX признаётся одинаковой, и всё это описывается
как процесс MX с тремя экземплярами работ. Дальше математика потока
работ через ресурс Васю. Проблемы появляются в тот момент, когда
выясняется, что кроме одинаковых работ у Васи есть куча самых разных
других работ, которые все разные у разных исполнителей. Процессное
управление тут говорит «если всё такое неодинаковое, то это к проектному
управлению, но наш одинаковый кусок у Васи мы бы обрабатывали именно
так, относясь к Васе как к станку». В теории массового обслуживания это
абсолютно нормально, там есть расхожий анекдот про общность постановки
задачи в самых разных ситуациях процессного управления: «к городу
подлетает эскадрилья бомбардировщиков, становясь в очередь на
обслуживание зенитной батареей».

Второй вариант начинается как раз с замечанием, что «если у вас всё
уникальное, то используйте управление проектами». Управление проектами
заболело теориями, что весь менеджмент (включая организационное
развитие, лидерство и сейчас даже обсуждается вопрос, что практика
ведения переговоров --- вот буквально всё, чем занимаются люди на
работе) это предмет проектного управления. Поэтому Вася для современных
проектных управляющих --- это не ресурс. Ему поручают одновременно все
проекты, и предупреждают, что строго спросят за все три. Типовая
ситуация многозадачности: Вася понимает, что ему и впрямь нужно будет
отчитываться за все три проекта. И он в первый день делает по 1/3
дневной нормы от каждого проекта. Через три дня у Васи выполнено работ
по каждому проекту на 1 день (чудес не бывает!), всего Вася трудился три
дня, все работы готовы на 10%. Директор звонит и интересуется, приступил
ли Вася к работе. Вася отвечает, что «да, движение по всем проектам». На
рисунке работа Васи показана как сплошная зелёная линия «занимается
проектом». Но в реальности каждая из этих линий будет пунктирна: один
такт работы по проекту, два такта работы нет (ибо идёт работа Васи по
двум другим проектам). На двадцатый день после попадания всех трёх работ
к Васе директор не выдерживает (его поджимают клиенты!) и звонит Васе.
Вася честно говорит, что все три проекта существенно продвинулись, на
две трети всё готово! Помним, что в предыдущем варианте Васи-станка
первый клиент к этому моменту (тридцатый день) получил результат своего
проекта, а работа по второму как раз у Васи закончилась. А в этом случае
«много проектов, и за все спрос» вроде как Вася не простаивал, третий
клиент всё одно ничего не получил, но и первый клиент не получил. В
последний тридцатый день Вася как «человек с порученными ему работами
многих проектов» отдаёт работы дальше по цепочке, и все три клиента
остаются несчастливы, хотя в случае васи-как-станка два клиента
счастливы в этот момент, а остальные только несчастливы. Тем самым
случай реализует «справедливость» как равномерное распределение
несчастья: третий клиент получал работу в первом случае на пятидесятый
день (ему не везло одному), а в случае Васи, нагруженного многими
проектами с обязательством «продвигаться по всем» все три клиента
оказываются «справедливо» в одинаковом положении, они несчастливы в
равной степени, счастливых нет. И при этом мы ещё считаем, что время
переключения Васи с работы на работу равно нулю! В жизни это никогда не
ноль, это время переключения добавляется к каждому такту каждой работы!

Есть ли пути улучшения этой ситуации? Да, есть. Нужно только заметить,
что «одинаковая работа» всё-таки занимает обычно разное время, но чаще
всего ровно столько, сколько запланировано (бывает, что позже, но
никогда не раньше). Если учесть статистику опозданий и запланировать
работу с риском неокончания её в этот укороченный срок, то можно
запланировать половину времени на работу, а половину времени поместить в
«буфер неокончания в запланированное время» в конце проекта. Если
спросить Васю, сколько он будет делать MX, то Вася ответит 10 дней ---
ибо считает, что это будет с вероятностью 99%. И он таки потратит все
десять дней! Но если ему дать на работу 8 дней, то он её завершит с
вероятностью, скажем, 90% именно в этот срок --- просто он для
надёжности добавляет дни в своей оценке). Если сделать это «укорочение
плана исходя из оценки 90% вероятности» с каждой работой, то можно
рассчитывать на тот же эффект, который используется в страховых
компаниях: проблемы будут не у всех работ, поэтому в реальности буфер
можно делать меньшей длины. На диаграмме показано, что вот этот вариант
с буферизацией за счёт учёта разницы во времени актуального выполнения
работ по сравнению с запланированным может сэкономить ещё пять дней даже
при использовании всего буфера проекта --- и первый клиент получит
результат через двадцать пять дней, а не через тридцать дней. Но буфер
совсем не обязательно будет использован весь, поэтому в реальности
результат может быть получен и на двадцатый день!

Беда в том, что это очень контринтуитивно: задействовать Васю как станок
и не давать «продвигаться по всем проектам», давать возможность работать
только с одним проектом «в силу арифметики». А уж что касается
использования буфера проекта и учёта тенденции завышать сроки работ, так
это и подавно контринтуитивно. Но управление работами основано ровно на
этой математике. **Многозадачность (когда кто-то одновременно выполняет
много работ из самых разных проектов) надо удавливать, она приводит к
резкому ухудшению результатов «из ниоткуда, чисто в силу формул».** **А
сами работы занимают время не столько, сколько** **для них
запланировано, и при этом не только больше запланированного, но и
меньше ---** **это даёт возможность буферизации во времени проекта (а
бывают ещё и другие буферизации ---** **например, буферизация ресурсов,
когда они сидят и ничего не делают, чтобы потом быть готовыми обслужить
пиковую нагрузку, типа как трёхрядная дорога простаивает на своих двух
полосах, пока не наступит час пик ---** **и тогда будут задействованы
все три полосы, чтобы не было стоячей пробки).**
