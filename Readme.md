### Счетчики покрытия тестами


INSTRUCTION

Позволит вам сделать общую проверку (например, убедитесь, что весь проект имеет по крайней мере 0.80 покрытия).
Самая маленькая единица измерения JaCoCo - это одиночные инструкции кода байта Java. Покрытие инструкции предоставляет информацию о количестве кода, который был выполнен или пропущен. Эта метрика полностью независима от исходного форматирования и всегда доступна даже в отсутствие отладочной информации в файлах классов.


BRANCH

JaCoCo также вычисляет охват веток для всех операторов if и switch. Эта метрика подсчитывает общее количество таких ветвей в методе и определяет количество выполненных или пропущенных ветвей. Распространение веток всегда доступно, даже при отсутствии отладочной информации в файлах классов. Обратите внимание, что обработка исключений не рассматривается как ветки в контексте этого определения счетчика.

Если файлы классов были скомпилированы с отладочной информацией, точки принятия решения могут быть сопоставлены с исходными строками и выделены соответствующим образом:

* Нет покрытия: нет ответвлений в линии (красный ромб)

* Частичное покрытие: выполнена только часть ветвей в линии (желтый ромб)

* Полное покрытие: все ответвления в линии выполнены (зеленый ромб)

LINE

Для всех файлов классов, которые были скомпилированы с отладочной информацией, можно рассчитать информацию о покрытии для отдельных строк. Исходная строка считается выполненной, если была выполнена хотя бы одна инструкция, назначенная этой строке.

В связи с тем, что одна строка обычно компилируется в инструкции с несколькими байтами, выделение исходного кода показывает три разных состояния для каждой строки,содержащей исходный код:

* Нет покрытия: ни одна инструкция в строке не была выполнена (красный фон)

* Частичное покрытие: выполнена только часть инструкции в строке (желтый фон)

Полное покрытие: все инструкции в строке выполнены (зеленый фон)

В зависимости от форматирования исходного кода одна строка исходного кода может относиться к нескольким методам или нескольким классам. Следовательно, количество строк методов нельзя просто добавить, чтобы получить общее количество для содержащего класса. То же самое верно и для строк нескольких классов в одном исходном файле. JaCoCo рассчитывает покрытие строк для классов и исходного файла на основе фактически охваченных строк исходного кода.
