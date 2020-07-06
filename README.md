<small>

## Java полное руководство - Герберт Шилдт, 10-е издание, 2018 г.

[Глава 6. "Введение в классы"](https://github.com/aykononov/JavaSchildt/tree/master/Chapter06/ "Chapter06")

[Глава 7. "Подробное рассмотрение классов и методов"](https://github.com/aykononov/JavaSchildt/tree/master/Chapter07/ "Chapter07")

<details><summary>Глава 8. "Наследование"</summary>

><details><summary>Основы наследования. (стр. 221)</summary>
>
>>Как только суперкласс, который определяет общие свойства объекта, будет создан, он может наследоваться для разработки специализированных классов. Каждый подкласс добавляет собственные особые характеристики. В этом и состоит вся суть наследования.
>>
>>[SimpleInheritance01 - Простой пример наследования](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/SimpleInheritance01.java)
>
></details>

><details><summary>Практический пример наследования. (стр. 224)</summary>
>
>>Если ссылочной переменной из Суперкласса присваивается ссылка на объект Подкласса, то доступ предоставляется только к указанным в ней частям объекта, определяемого в Суперклассе, потому-что Суперклассу неизвестно, что именно добавляет в него Подкласс.
>>
>>[DemoBoxWeight02 - Пример, где наследование применяется для расширения класса](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/DemoBoxWeight02.java)
>
></details>

><details><summary>Вызов конструкторов Суперкласса с помощью ключевого слова super. (стр. 227)</summary>
>
>>При вызове метода super() из Подкласса вызывается конструктор его непосредственного Суперкласса. Таким образом, метод super() всегда обращается к Суперклассу, находящемуся в иерархии непосредственно над вызывающим классом. Это справедливо даже для многоуровневой иерархии. Кроме того, вызов метода super() должен быть непременно сделан в первом операторе, выполняемом в теле конструктора Подкласса.
>>
>>[DemoBoxWeight03 - Вызов конструкторов Суперкласса с помощью ключевого слова super](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/DemoBoxWeight03.java)
>
></details>

><details><summary>Посмотрим на ссылочные переменные...</summary>
>
>>Можно посмотреть и сравнить, как выглядят ссылочные переменные при клонировании объектов и копировании ссылок на объекты.
>>
>>[ReferenceVariables04 ](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/ReferenceVariables04.java)
>
></details>

><details><summary>Создание многоуровневой иерархии. (стр. 232)</summary>
>
>>Каждый Подкласс наследует все характеристики всех его Суперклассов. Подкласс BoxWeight служит в качестве Суперкласса для создания Подкласса BoxShipment и добавляет к ним поле cost. Благодаря наследованию в классе BoxShipment можно использовать ранее определенные классы Вох и BoxWeight, добавляя только те дополнительные данные, которые требуются для его собственного специализированного применения. В этом и состоит одна из самых ценных особенностей наследования. Она позволяет использовать код повторно. Приведенный пример демонстрирует еще одну важную особенность наследования: метод super() всегда ссылается на конструктор ближайшего по иерархии Суперкласса. В методе super() из класса BoxSlipment вызывается конструктор класса BoxWeight. А в методе super() из класса BoxWeight вызывается конструктор класса Вох. Если в иерархии классов требуется передать параметры конструктору Cуперкласса, то все подклассы должны передавать эти параметры вверх по иерархии. Данное утверждение справедливо независимо от того, нуждается ли Подкласс в собственных параметрах.
>>
>>[DemoShipment05 - Пример, создания многоуровневой иерархии](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/DemoShipment05.java)
>
></details>

><details><summary>Порядок вызова конструкторов. (стр. 235)</summary>
>
>>В иерархии классов конструкторы вызываются в порядке наследования, начиная с суперкласса и кончая подклассом. Более того, этот порядок остается неизменным независимо от того, используется форма super() или нет, поскольку вызов метода super() должен быть в первом операторе, выполняемом в конструкторе подкласса. Если метод super() не вызывается, то используется конструктор по умолчанию или же конструктор без параметров из каждого суперкласса.
>>
>>[CallingConstr06 - Порядок вызова конструкторов](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/CallingConstr06.java)
>
></details>

><details><summary>Переопределение методов. (стр. 236)</summary>
>
>>Если в иерархии классов совпадают имена и сигнатуры типов методов из Подкласса и Суперкласса, то говорят, что метод из Подкласса переопределяет метод из Суперкласса. Когда переопределенный метод вызывается из своего Подкласса, он всегда ссылается на свой вариант, определенный в Подклассе. А вариант метода, определенный в Суперклассе, будет скрыт.
>>
>>[OverrideMethod07 - Пример, переопределения методов](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/OverrideMethod07.java)
>
></details>

><details><summary>Перегрузка методов. (стр. 238)</summary>
>
>>Переопределение методов выполняется только в том случае, если имена и сигнатуры типов обоих методов одинаковы. В противном случае оба метода считаются перегружаемыми.
>>
>>[OverloadMethod08 - Пример, перегрузки методов](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/OverloadMethod08.java)
>
></details>

><details><summary>Динамическая диспетчеризация методов. (стр. 239)</summary>
>
>>Динамическая диспетчеризация методов - это механизм, с помощью которого вызов переопределенного метода разрешается во время выполнения, а не компиляции.
>>Ссылочная переменная из Суперкласса может ссылаться на объект Подкласса. Когда переопределенный метод вызывается по ссылке на Суперкласс, нужный вариант этого метода выбирается в Java в зависимости от типа объекта, на который делается ссылка в момент вызова.
>>
>>В этом примере создаются один Суперкласс А и два его Подкласса В и С. В Подклассах В и С переопределяется метод callme(), объявляемый в классе А. В методе main() объявляются объекты классов А, В и С, а также переменная ref ссылки на объект типа А. Затем переменной ref присваивается по очереди ссылка на объект каждого из классов А, В и С, и по этой ссылке вызывается метод callme().
>>Как следует из результата, выводимого этой программой, выполняемый вариант метода callme() определяется исходя из типа объекта, на который делается ссылка в момент вызова. Если бы выбор делался по типу ссылочной переменной ref, то выводимый результат отражал бы три вызова одного и того же метода callme() из класса А.
>>
>>[DynamicMethodDispatching09 - Динамическая диспетчеризация методов](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/DynamicMethodDispatching09.java)
>
></details>

><details><summary>Назначение и Применение переопределенных методов. (стр. 240 - 241)</summary>
>
>>Переопределенные методы позволяют поддерживать в Java полиморфизм во время выполнения. Это позволяет определить в общем классе методы, которые станут общими для всех производных от него классов, а в подклассах - конкретные реализации некоторых или всех этих методов.
>>Переопределенные методы предоставляют еще один способ реализовать в Java принцип полиморфизма "один интерфейс, множество методов".
>>Одним из основных условий успешного применения полиморфизма является ясное понимание, что суперклассы и подклассы образуют иерархию по степени увеличения специализации. Если суперкласс применяется правильно, он предоставляет все элементы, к<?торые могут непосредственно использоваться в подклассе. В нем также определяются те методы, которые должны быть реализованы в самом производном классе. Это дает удобную возможность определять в подклассе его собственные методы, сохраняя единообразие интерфейса. Таким образом, сочетая наследование с переопределенными методами, в суперклассе можно определить общую форму для методов, которые будут использоваться во всех его подклассах.
>>Динамический полиморфизм, реализуемый во время выполнения, это один из самых эффективных механизмов объектно-ориентированной архитектуры, обеспечивающих повторное использование и надежность кода. Возможность вызывать из библиотек уже существующего кода методы для экземпляров новых классов, не прибегая к повторной компиляции и в то же время сохраняя ясность абстрактного интерфейса, является сильнодействующим средством.
>>Практический пример, в котором применяется переопределение методов. В приведенной ниже программе создается суперкласс Figure для хранения размеров двумерного объекта, а также определяется метод area() для расчета площади этого объекта. Кроме того, в этой программе создаются два класса,
>>Rectangle и Triangle, производные от класса Figure. Метод area() переопределяется в каждом из этих подклассов, чтобы возвращать площадь четырехугольника и треугольника соответственно.
>>   
>>[FigureFindArea10 - Применение динамического полиморфизма](https://github.com/aykononov/JavaSchildt/blob/master/Chapter08/FigureFindArea10.java)
>
></details>

</details>

</small>