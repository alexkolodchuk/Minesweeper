# Minesweeper
Проект "Сапёр" на Python 3.

Аналог Сапёра (Minesweeper) на языке Python 3.8.2.
Ничего сложного.

В программе всё расписано подробно.

Вся программа построена на огромном списке с вложенными списками с вложенными списками. Каждая клетка - список с 3-мя значениями.
Например, ['0', ' ', 'c'].
Первое значение - либо '0', либо '1'. Это значит, есть ли в клетке бомба или нет.
Это значение генерируется рандомно по карте согласно параметрам.
Второе значение - сколько бомб вокруг клетки. Если 0, то пишет ' '.
Третье значение - режим клетки. 'c' - значит 'closed', 'закрыта'.
'o' - значит 'opened', 'открыта'. 'f' - значит 'flagged', 'помечена'.
Собираются все списки в одной строке в ещё один большой список. А потом все
строки по порядку - в последний. Итак, чтобы добраться до клетки, нужно написать
список[y][x]. Соответственно три значения получаются прибавлением [0], [1] и [2].

Один большой список со вложенными списками со вложенными списками.
Вложенные списки в большой - это строки. Каждый подвложенный список - клетка.
Для клетки нужно: минное значение, режим, заминирована ли.
Минное значение: от '1' до '8' и ' ' для '0'.
Режим:
  'c' ('closed') - нераскрытая клетка. 
  'o' ('opened') - раскрытая клетка. Открывается вбиванием координат.
  'f' ('flagged') - помеченная флажком клетка. Открывается вбиванием координат и символа "F"/"f".
То есть список для 1 клетки такой: ['3', 'closed', '1'] - около неё 3 мины, клетка закрыта, клетка заминирована.
