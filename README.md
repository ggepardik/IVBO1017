Техническое задание
N.N.00011-01 ТЗ 013-КЕ
СОДЕРЖАНИЕ
1. ВВЕДЕНИЕ
1.1. Наименование программы
1.2. Краткая характеристика области применения программы
2. ОСНОВАНИЕ ДЛЯ РАЗРАБОТКИ
2.1. Основание для проведения разработки
2.2. Наименование и условное обозначение темы разработки
3. НАЗНАЧЕНИЕ РАЗРАБОТКИ
3.1. Функциональное назначение программы
3.2. Эксплуатационное назначение программы
4. ТРЕБОВАНИЯ К ПРОГРАММЕ
4.1. Требования к функциональным характеристикам
4.1.1. Требования к составу выполняемых функций
4.1.2. Требования к организации входных и выходных данных
4.1.3. Требования к временным характеристикам
4.2. Требования к надежности
4.2.1. Требования к обеспечению надежного (устойчивого) функционирования программы
4.2.2. Контроль входной и выходной информации
4.2.3. Время восстановления после отказа
4.3. Условия эксплуатации
4.3.1. Климатические условия эксплуатации
4.3.2. Требования к видам обслуживания
4.3.3. Требования к численности и квалификации персонала
4.4. Требования к составу и параметрам технических средств
4.5. Требования к информационной и программной совместимости
4.5.1. Требования к информационным структурам и методам решения
4.5.2. Требования к исходным кодам и языкам программирования
4.5.3. Требования к программным средствам, используемым программой
4.5.4. Требования к защите информации и программ
4.6. Требования к маркировке и упаковке
4.7. Требования к транспортированию и хранению
4.8. Специальные требования
5. ТРЕБОВАНИЯ К ПРОГРАММНОЙ ДОКУМЕНТАЦИИ
5.1. Предварительный состав программной документации
5.2. Специальные требования к программной документации
6. ТЕХНИКО-ЭКОНОМИЧЕСКИЕ ПОКАЗАТЕЛИ
6.1. Ориентировочная экономическая эффективность
6.2. Предполагаемая годовая потребность
6.3. Экономические преимущества разработки
7. СТАДИИ И ЭТАПЫ РАЗРАБОТКИ
7.1. Стадии разработки
7.2. Этапы разработки
7.3. Содержание работ по этапам
8. ПОРЯДОК КОНТРОЛЯ И ПРИЕМКИ
8.1. Виды испытаний
8.2. Общие требования к приемке работы
1. ВВЕДЕНИЕ
1.1. Наименование программы
Наименование – «Утилита CALL командной строки CMD»
1.2. Краткая характеристика области применения программы
Оператор CALL Передает управление в процедуру Sub , Function или процедуру библиотеки динамической компоновки (DLL) ..

2. ОСНОВАНИЕ ДЛЯ РАЗРАБОТКИ
2.1. Основание для проведения разработки
Основанием для проведения разработки является лабораторный практикум по дисциплине «Технология разработки ПО АСОИУ», утвержденный Сувальским А.А., в дальнейшем именуемым Заказчиком. Дата утверждения – 03.09.2020.
2.2. Наименование и условное обозначение темы разработки
Наименование темы разработки – «Разработка утилиты CALL.
Условное обозначение темы разработки – «N.N.00011».
3. НАЗНАЧЕНИЕ РАЗРАБОТКИ
3.1. Функциональное назначение программы
Ключевое слово Call не требуется обязательно использовать при вызове процедуры. Однако если ключевое слово Call используется для вызова процедуры, требующей задания аргументов, элемент список_аргументов должен быть заключен в скобки. Если ключевое слово Call будет пропущено, необходимо также убрать и скобки вокруг элемента список_аргументов. Если используется синтаксис Call для вызова любой внутренней либо определяемой пользователем функции, значение, возвращаемое этой функцией, отбрасывается. Чтобы передать процедуре целый массив, используйте имя этого массива, после которого следует записать пустые скобки.

3.2. Эксплуатационное назначение программы
Утилита CALL должна эксплуатироваться в интерпретаторе командной строки CMD или в пакетном файле.
4. ТРЕБОВАНИЯ К ПРОГРАММЕ
4.1. Требования к функциональным характеристикам
4.1.1. Требования к составу выполняемых функций
Утилита CALL должна обеспечивать возможность выполнения перечисленных ниже функций:
1.	выполнять точный поиск текста в любом текстовом файле или файлах формата ASCII;
2.	предоставлять возможность поиска с использованием регулярных выражений; 
3.	предоставлять использование как литеральных символов, так и мета-символов.
4.1.2. Требования к организации входных и выходных данных
Синтаксис
Синтаксис оператора Call состоит из следующих частей:

ПАРАМЕТРЫ ПАКЕТА
Параметр Batch Описание

1 Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.
В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов. ПАРАМЕТРЫ ПАКЕТА

|Параметр Batch| Описание
| ------------ | ------------ |
| % ~ 1 | Развертывает %1 и удаляет окружающие кавычки.
|% ~ F1|  Расширение %1 до полного пути.
| % ~D1 |  Расширение %1 до буквы диска.
| % ~ P1|  Развертывает %1 только для пути.
| % ~N1| Расширение %1 только на имя файла.
| % ~ x1|  Развертывает %1 только для расширения имени файла.
| % ~S1 | Расширение %1 до полного пути, содержащего только короткие имена.
| % ~ a1|  Развертывает %1 для атрибутов файла.
|  % ~T1 | Увеличивает %1 до даты и времени файла.
| % ~ Z1 | Расширение %1 до размера файла.
| %~$PATH: 1|  Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.

В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов.

**ТАБЛИЦА 2**

|Параметр Batch с модификатором | Описание
| ------------ | ------------ |
|% ~ DP1| Расширение %1 до буквы диска и пути.
|% ~ nx1| Развертывает %1 только для имени файла и расширения.
|% ~ точка DP $ PATH: 1| Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
|% ~ ftza1 | Разворачивает %1 для вывода выходных данных, аналогичных команде dir .

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с % *. 

**ТАБЛИЦА 3**

|Параметр Batch с модификатором | Описание
| ------------ | ------------ |
|% ~ DP1| Расширение %1 до буквы диска и пути.
|% ~ nx1| Развертывает %1 только для имени файла и расширения.
|% ~ точка DP $ PATH: 1| Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
|% ~ ftza1 | Разворачивает %1 для вывода выходных данных, аналогичных команде dir

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с % *.
Ссылки на аргумент скрипта пакетной службы (%0, %1,...) перечислены в следующих таблицах. Ссылки на аргумент скрипта пакетной службы (%0, %1,...) перечислены в следующих таблицах.
Использование значения % * в пакетном скрипте означает все аргументы (например, %1, %2, %3...). Использование значения % * в пакетном скрипте означает все аргументы (например, %1, %2, %3...).
Можно использовать следующие необязательные синтаксисы в качестве подстановок для пакетных параметров (% n): Можно использовать следующие необязательные синтаксисы в качестве подстановок для пакетных параметров (% n):
ПАРАМЕТРЫ ПАКЕТА

|Параметр Batch| Описание
| ------------ | ------------ |
|% ~ 1 | Развертывает %1 и удаляет окружающие кавычки.
|% ~ F1| Расширение %1 до полного пути.
|% ~ D1 |Расширение %1 до буквы диска.
|% ~ P1| Развертывает %1 только для пути.
|% ~ N1| Расширение %1 только на имя файла.
|% ~ x1| Развертывает %1 только для расширения имени файла.
|% ~ S1| Расширение %1 до полного пути, содержащего только короткие имена.
|% ~ a1| Развертывает %1 для атрибутов файла.
|% ~ T1| Увеличивает %1 до даты и времени файла.
|% ~ Z1| Расширение %1 до размера файла.
|% ~ $PATH: 1| Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.

В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов. ПАРАМЕТРЫ ПАКЕТА

|Параметр Batch| Описание
| ------------ | ------------ |
|% ~ 1| Развертывает %1 и удаляет окружающие кавычки.
|% ~ F1| Расширение %1 до полного пути.
|% ~ D1| Расширение %1 до буквы диска.
|% ~ P1 |Развертывает %1 только для пути.
|% ~ N1| Расширение %1 только на имя файла.
|% ~ x1|Развертывает %1 только для расширения имени файла.
|% ~ S1| Расширение %1 до полного пути, содержащего только короткие имена.
|% ~ a1| Развертывает %1 для атрибутов файла.
|% ~ T1| Увеличивает %1 до даты и времени файла.
|% ~ Z1| Расширение %1 до размера файла.
|% ~ $PATH: 1 |Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.

В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов.
**ТАБЛИЦА 4**

|Параметр Batch с модификатором| Описание
| ------------ | ------------ |
|% ~ DP1 |Расширение %1 до буквы диска и пути.
|% ~ nx1 |Развертывает %1 только для имени файла и расширения.
|% ~ точка DP $ PATH: 1| Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
|% ~ ftza1| Разворачивает %1 для вывода выходных данных, аналогичных команде dir .

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с %.

|Параметр Batch с модификатором| Описание
| ------------ | ------------ |
|% ~ DP1| Расширение %1 до буквы диска и пути.
|% ~ nx1| Развертывает %1 только для имени файла и расширения.
|% ~ точка DP $ PATH: 1| Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
|% ~ ftza1| Разворачивает %1 для вывода выходных данных, аналогичных команде dir .

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с % *.
Ссылки на аргумент скрипта пакетной службы (%0, %1,...) перечислены в следующих таблицах. Ссылки на аргумент скрипта пакетной
 
службы (%0, %1,...) перечислены в следующих таблицах.
Использование значения % * в пакетном скрипте означает все аргументы (например, %1, %2, %3...). Использование значения % * в пакетном скрипте означает все аргументы (например, %1, %2, %3...).
Можно использовать следующие необязательные синтаксисы в качестве подстановок для пакетных параметров (% n): Можно использовать следующие необязательные синтаксисы в качестве подстановок для пакетных параметров (% n):
ПАРАМЕТРЫ ПАКЕТА

|Параметр Batch| Описание
| ------------ | ------------ |
| % ~ 1|  Развертывает %1 и удаляет окружающие кавычки.
| % ~ F1|  Расширение %1 до полного пути.
| % ~ D1 | Расширение %1 до буквы диска.
| % ~ P1|  Развертывает %1 только для пути.
| % ~ N1|  Расширение %1 только на имя файла.
| % ~ x1|  Развертывает %1 только для расширения имени файла.
| % ~ S1|  Расширение %1 до полного пути, содержащего только короткие имена.
| % ~ a1 | Развертывает %1 для атрибутов файла.
| % ~ T1|  Увеличивает %1 до даты и времени файла.
| % ~ Z1|  Расширение %1 до размера файла.
| % ~ $PATH: 1 | Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.

В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов. ПАРАМЕТРЫ ПАКЕТА

|Параметр Batch| Описание
| ------------ | ------------ |
|% ~ 1| Развертывает %1 и удаляет окружающие кавычки.
|% ~ F1 | асширение %1 до полного пути.
|% ~ D1| Расширение %1 до буквы диска.
|% ~ P1| Развертывает %1 только для пути.
|% ~ N1| Расширение %1 только на имя файла.
|% ~ x1| Развертывает %1 только для расширения имени файла.
|% ~ S1| Расширение %1 до полного пути, содержащего только короткие имена.
|% ~ a1| Развертывает %1 для атрибутов файла.
|% ~ T1| Увеличивает %1 до даты и времени файла.
|% ~ Z1| Расширение %1 до размера файла.
|% ~ $PATH: 1| Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.

В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов.

**ТАБЛИЦА 5**

|Параметр Batch с модификатором | Описание
| ------------ | ------------ |
| % ~ DP1|  Расширение %1 до буквы диска и пути.
| % ~ nx1|  Развертывает %1 только для имени файла и расширения.
| % ~ точка DP $ PATH: 1 | Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
| % ~ ftza1|  Разворачивает %1 для вывода выходных данных, аналогичных команде dir .

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с % *. ТАБЛИЦА 3

|Параметр Batch с модификатором| Описание
| ------------ | ------------ |
| % ~ DP1 | Расширение %1 до буквы диска и пути.
| % ~ nx1|  Развертывает %1 только для имени файла и расширения.
| % ~ точка DP $ PATH: 1 | Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
| % ~ ftza1 | Разворачивает %1 для вывода выходных данных, аналогичных команде dir .

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с % *.
Ссылки на аргумент скрипта пакетной службы (%0, %1,...) перечислены в следующих таблицах. Ссылки на аргумент скрипта пакетной службы (%0, %1,...) перечислены в следующих таблицах.
Использование значения % * в пакетном скрипте означает все аргументы (например, %1, %2, %3...). Использование значения % * в пакетном скрипте означает все аргументы (например, %1, %2, %3...).
Можно использовать следующие необязательные синтаксисы в качестве подстановок для пакетных параметров (% n): Можно использовать следующие необязательные синтаксисы в качестве подстановок для пакетных параметров (% n):
ПАРАМЕТРЫ ПАКЕТА

|Параметр Batch| Описание
| ------------ | ------------ |
| % ~ 1 | Развертывает %1 и удаляет окружающие кавычки.
| % ~ F1 |  Расширение %1 до полного пути.
| % ~ D1 |  Расширение %1 до буквы диска.
| % ~ P1 |  Развертывает %1 только для пути.
| % ~ N1 |  Расширение %1 только на имя файла.
| % ~ x1|  Развертывает %1 только для расширения имени файла.
| % ~ S1|  Расширение %1 до полного пути, содержащего только короткие имена.
| % ~ a1|  Развертывает %1 для атрибутов файла.
| % ~ T1|  Увеличивает %1 до даты и времени файла.
| % ~ Z1|  Расширение %1 до размера файла.
| % ~ $PATH: 1|  Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.
В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов. ПАРАМЕТРЫ ПАКЕТА

|Параметр Batch| Описание
| ------------ | ------------ |
| % ~ 1 |  Развертывает %1 и удаляет окружающие кавычки.
| % ~ F1 |   Расширение %1 до полного пути.
| % ~ D1 |  Расширение %1 до буквы диска.
| % ~ P1 |  Развертывает %1 только для пути.
| % ~ N1|   Расширение %1 только на имя файла.
| % ~ x1|   Развертывает %1 только для расширения имени файла.
| % ~ S1 |  Расширение %1 до полного пути, содержащего только короткие имена.
| % ~ a1|  Развертывает %1 для атрибутов файла.
| % ~ T1|  Увеличивает %1 до даты и времени файла.
| % ~ Z1|  Расширение %1 до размера файла.
| % ~ $PATH: 1|  Выполняет поиск в каталогах, перечисленных в переменной среды PATH, и разворачивает %1 до полного имени найденного первого каталога. Если имя переменной среды не определено или файл не найден при поиске, то этот модификатор разворачивается до пустой строки.
В следующей таблице показано, как можно объединить модификаторы с пакетными параметрами для составных результатов.


ТАБЛИЦА 6
|Параметр Batch с модификатором| Описание
| ------------ | ------------ |
| % ~ DP1 | Расширение %1 до буквы диска и пути.
| % ~ nx1   Развертывает |%1 только для имени файла и расширения.
| % ~ точка DP $ PATH: 1|  Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
| % ~ ftza1|  Разворачивает %1 для вывода выходных данных, аналогичных команде dir .

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с % *.

|Параметр Batch с модификатором| Описание
| ------------ | ------------ |
| % ~ DP1 | Расширение %1 до буквы диска и пути.
| % ~ nx1 Развертывает %1|  только для имени файла и расширения.
| % ~ точка DP $ PATH: 1|  Выполняет поиск в каталогах, перечисленных в переменной среды PATH для %1, а затем разворачивается на букву диска и путь к первому найденному каталогу.
| % ~ ftza1 | Разворачивает %1 для вывода выходных данных, аналогичных команде dir .

В приведенных выше примерах %1 и Path могут быть заменены другими допустимыми значениями. %~ Синтаксис завершается допустимым номером аргумента. %~ Модификаторы нельзя использовать с % *.
Ссылки на аргумент скрипта пакетной службы (%0, %1,...) перечислены в следующих таблицах. Ссылки на аргумент скрипта пакетной службы (%0, %1,...) перечислены в следующих таблицах.

4.1.3. Требования к временным характеристикам
Требования к временным характеристикам программы не предъявляются.
4.2. Требования к надежности
4.2.1. Требования к обеспечению надежного (устойчивого) функционирования программы
Надежное (устойчивое) функционирование программы должно быть обеспечено выполнением совокупности организационно-технических мероприятий:
1. организацией бесперебойного питания технических средств;
2. выполнением рекомендаций Министерства труда и социального развития РФ, изложенных в Постановлении от 23 июля 1998 г. «Об утверждении межотраслевых типовых норм времени на работы по сервисному обслуживанию ПЭВМ и оргтехники и сопровождению программных средств»;
3. выполнением требований ГОСТ 51188-98. Защита информации. Испытания программных средств на наличие компьютерных вирусов;
4. необходимым уровнем квалификации сотрудников профильных
 
подразделений.
4.2.2. Контроль входной и выходной информации
Предусмотреть блокировку некорректных действий пользователя при работе с системой – вывод сообщения об ошибке с вводом.
4.2.3. Время восстановления после отказа
Время восстановления после отказа должно не превышать 20 мин.
4.3. Условия эксплуатации
4.3.1. Климатические условия эксплуатации
Программа должна работать в закрытых помещениях, при нормальных климатических условиях.
Температура окружающего воздуха должна быть в диапазоне 20-30 градусов, относительная влажность на уровне 40-60%.
4.3.2. Требования к видам обслуживания
Проводится периодическое тестирование программы, раз в полгода.
4.3.3. Требования к численности и квалификации персонала
Минимальное количество персонала, требуемого для работы программы, должно составлять не менее двух штатных единиц – системный администратор и конечный пользователь программы – оператор.
Системный администратор должен иметь минимум среднее техническое образование. В перечень задач, выполняемых системным администратором, должны входить:
1. задача поддержания работоспособности технических средств;
2. задача установки (инсталляции) и поддержания работоспособности системного программного средства - операционной системы;
3. задача установки (инсталляции) программы.
Конечный пользователь программы (оператор) должен обладать практическими навыками работы с графическим пользовательским интерфейсом операционной системы.
4.4. Требования к составу и параметрам технических средств
B состав технических средств должен входить IBM-совместимый персональный компьютер (ПЭВМ), включающий в себя:
1. процессор Pentium – 4 с тактовой частотой не менее 300 МГц;
2. оперативную память объемом не менее 128 Мб;
3. жесткий диск объемом 1.5 Гб и выше.
4. система должна работать под управлением семейства операционных систем Win 32 (Windows 95, Windows 98, Windows 2000, Windows NT и т. п.).
4.5. Требования к информационной и программной совместимости
4.5.1. Требования к информационным структурам и методам решения
Требования к информационным структурам на входе и выходе, а также к методам решения не предъявляются.
4.5.2. Требования к исходным кодам и языкам программирования
Исходные коды программы должны быть реализованы в пакетном файле или непосредственно в интерпретаторе командной строки CMD.
4.5.3. Требования к программным средствам, используемым программой
Должна использоваться командная строка, встроенная в операционную систему Windows.
4.5.4. Требования к защите информации и программ
Требования к защите информации и программ не предъявляются.
4.6. Требования к маркировке и упаковке
Требования к маркировке и упаковке не предъявляются.
4.7. Требования к транспортированию и хранению
Требования к транспортированию и хранению не предъявляются.
4.8. Специальные требования
Специальные требования к программе не предъявляются.
5. ТРЕБОВАНИЯ К ПРОГРАММНОЙ ДОКУМЕНТАЦИИ
5.1. Предварительный состав программной документации
Состав программной документации должен включать в себя:
• техническое задание;
• спецификация;
• текст программы;
• описание программы;
• программу и методики испытаний;
• пояснительную записку;
• ведомость эксплуатационных документов;
• формуляр;
• описание применения;
• руководство системного программиста;
• руководство программиста;
• руководство оператора.
5.2. Специальные требования к программной документации
Специальные требования к программной документации не предъявляются.
6. ТЕХНИКО-ЭКОНОМИЧЕСКИЕ ПОКАЗАТЕЛИ
6.1. Ориентировочная экономическая эффективность
Ориентировочная экономическая эффективность не рассчитывается.
6.2. Предполагаемая годовая потребность
Предполагаемая годовая потребность не рассчитывается.
6.3. Экономические преимущества разработки
Экономические преимущества разработки не рассчитываются.
7. СТАДИИ И ЭТАПЫ РАЗРАБОТКИ
7.1. Стадии разработки
Разработка должна быть проведена в три стадии:
1. разработка технического задания;
2. рабочее проектирование;
3. внедрение.
7.2. Этапы разработки
На стадии разработки технического задания должен быть
 
выполнен этап разработки, согласования и утверждения между Заказчиком и Исполнителем настоящего технического задания.
На стадии рабочего проектирования должны быть выполнены следующие этапы работ:
1. разработка программы;
2. разработка программной документации;
3. испытания программы.
На стадии внедрения должен быть выполнен этап разработки – подготовка и передача программы.
7.3. Содержание работ по этапам
На этапе разработки технического задания должны быть выполнены следующие виды работ:
1. постановка задачи;
2. определение и уточнение требований к техническим средствам;
3. определение требований к программе;
4. определение стадий, этапов и сроков разработки программы и документации на неё;
5. выбор языков программирования;
6. согласование и утверждение технического задания.
На этапе разработки программы должна быть выполнена работа по программированию и отладке программы.
На этапе разработки программной документации должна быть выполнена разработка программных документов в соответствии с требованиями ГОСТ 19. 101-77 и требованием п. «Предварительный состав программной документации» настоящего технического задания.
На этапе испытаний программы должны быть выполнены следующие виды работ:
1. разработка, согласование и утверждение программы и методики испытаний;
2. проведение приемо-сдаточных испытаний;
3. корректировка программы и программной документации по результатам испытаний.
На этапе подготовки и передачи программы должна быть выполнена работа по подготовке и передаче программы и программной документации в эксплуатацию на объектах Заказчика.
8. ПОРЯДОК КОНТРОЛЯ И ПРИЕМКИ
8.1. Виды испытаний
Приемо-сдаточные испытания программы должны проводиться согласно разработанной Исполнителем и согласованной Заказчиком «Программы и методики испытаний».
Ход проведения приемо-сдаточных испытаний документируется Заказчиком и Исполнителем в Протоколе проведения испытаний.
8.2. Общие требования к приемке работы
После проведения испытаний в полном объеме, на основании «Протокола испытаний» утверждают «Свидетельство о приемке» и производят запись в программном документе «Формуляр»
