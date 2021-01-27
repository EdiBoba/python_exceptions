# Иерархия исключений стандартной библиотеки

*взято из документации Python 3.9*

- **BaseException** - базовый класс для всех встроенных исключений
    - **SystemExit** - бросает функция sys.exit при выходе из программы
    - **KeyboardInterrupt** - прерывании программы пользователем (Ctrl + C)
    - **GeneratorExit** - при вызове метода close объекта generator
    - **Exception** - базовый класс для не системных исключений
        - **StopIteration** - бросает next, если достигнут конец итератора
        - **StopAsyncIteration** - то же самое, только для асинхронного генератора
        - **ArithmeticError** - ошибка при арифметической операции
            - **FloatingPointError** - исключение, возникающее при ошибках во время операций с числами с плавающей запятой. Практически никогда
            - **OverflowError** - когда результат арифметической операции слишком велик для представления
            - **ZeroDivisionError** - ошибка при делении на ноль
        - **AssertionError** - выражение в функции assert ложно
        - **AttributeError** - объект не имеет данного атрибута (значения или метода)
        - **BufferError** - когда операция, тем или иным образом связанная с буфером, не может быть выполнена
        - **EOFError** - Поднимается встроенными функциями, например, input() и raw_input(), когда те обнаруживают маркер конца файла (EOF) в данных
        - **ImportError** - когда инструкции import не удаётся отыскать модуль, либо когда from ... import ... не находит атрибута, который требуется импортировать
            - **ModuleNotFoundError** - когда не удается отыскать модуль
        - **LookupError** - базовое исключение для ошибок доступа по ключу/индексу
            - **IndexError** - при обращении к элементу по индексу, находящемуся вне диапазона
            - **KeyError** - при обращении к элементу по ключу, отсутствующему в отображении
        - **MemoryError** - в некритичных случаях исчерпания свободной памяти
        - **NameError** - глобальное или локальное имя не найдено
            - **UnboundLocalError** - при обращении к локальной переменной, которая не была определена
        - **OSError** - базовый класс для системных ошибок
            - **BlockingIOError** - в случаях блокировки ввода-вывода
            - **ChildProcessError** - в случае ошибок в дочернем процессе
            - **ConnectionError** - базовый класс для исключений, связанных с проблемами соединений
                - **BrokenPipeError** - для ошибок соединения при работе с каналами
                - **ConnectionAbortedError** - в случае завершения узлом соединения
                - **ConnectionRefusedError** - в случае отказа узла в попытке соединения
                - **ConnectionResetError** - в случае сброса узлом соединения
            - **FileExistsError** - в случае попыток создать уже существующий файл, либо директорию
            - **FileNotFoundError** - в случае обращения к несуществующему файлу, либо директории
            - **InterruptedError** - в случае прерывания системного вызова сигналом
            - **IsADirectoryError** - в случае попытки применения к директории операции предназначенной для файлов
            - **NotADirectoryError** - в случае попытки применения к не директории операции предназначенной для директории
            - **PermissionError** - в случае попытки запуска операции без достаточных для этого прав
            - **ProcessLookupError** - в случае попытки обращения к несуществующему процессу
            - **TimeoutError** - в случае обрыва исполнения системной функции из-за таймаута на системном уровне
        - **ReferenceError** - при попытке обращения к атрибуту объекта через слабую ссылку, когда упомянутый объект уже недоступен
        - **RuntimeError** - ошибку времени исполнения не попадающую в другие категории
            - **NotImplementedError** - в случаях, когда наследник класса не переопределил метод, который должен был
            - **RecursionError** - в случае обнаружения рекурсивного вызова
        - **SyntaxError** - при обнаружении синтаксических ошибок в исходном коде
            - **IndentationError** - в случаях ошибок отступа
                - **TabError** - в случае смешивания различных символов для отступа
        - **SystemError** - в случаях ошибок уровня интерпретатора
        - **TypeError** - при попытке манипуляции объектом не поддерживающим такого рода манипуляцию
        - **ValueError** - в случаях, когда в функцию передан аргумент с неподдерживаемым значением
            - **UnicodeError** - ошибка, связанная с кодированием/раскодированием unicode в строках
                - **UnicodeDecodeError** - исключение, связанное с кодированием unicode
                - **UnicodeEncodeError** - исключение, связанное с декодированием unicode
                - **UnicodeTranslateError** - исключение, связанное с переводом unicode
        - **Warning** - базовый класс исключений-предупреждений
            - **DeprecationWarning** - для указания на то, что функциональность уже морально устарела
            - **PendingDeprecationWarning** - для указания на то, что функциональность морально устареет в скором времени
            - **RuntimeWarning** - предупреждение о сомнительном поведении во время исполнения
            - **SyntaxWarning** - предупреждение об использовании сомнительных синтаксических конструкций
            - **UserWarning** - пользовательские предупреждений
            - **FutureWarning** - предупреждения об изменениях в будущем
            - **ImportWarning** - предупреждение о вероятной ошибке при импорте модуля
            - **UnicodeWarning** - предупреждения, связанные с возможными проблемами при работе с unicode
            - **BytesWarning** - предупреждения, связанные с возможными проблемами при работе с байтами
            - **ResourceWarning** - предупреждения, связанные с возможными проблемами при работе с ресурсами

*информация взята с сайтов: https://pythonz.net/ и https://pythonworld.ru/*