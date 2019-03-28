
######################
Не забываем о названии
######################


.. image:: files/some_pics/corrected.jpg
   :height: 100px
   :width: 200 px
   :scale: 50 %


.. csv-table:: Таблица давай!!!
  :file: files/newCSV.csv
  :widths:  1, 7, 12, 41
  :header-rows: 1
  :stub-columns: 1







допустим я напишу сюда Сабака_ (и это выражение должно быть ссылкой на википедию, как и `Кошка <https://ru.wikipedia.org/wiki/%D0%9A%D0%BE%D1%88%D0%BA%D0%B0>`__)

.. _Сабака: https://ru.wikipedia.org/wiki/%D0%A1%D0%BE%D0%B1%D0%B0%D0%BA%D0%B0


пробел
пробел
пробел
пробел
пробелпробе

переход на единичку лось_

.. _лось:

ой сматри: мы перешли не на цифру, а на эти буквы! ВАУ а тут еще и ссылки всякие валяются в тупую: http://www.python.org ! 

Далее тут нужно вставить новый csv, в котором будет внутрення ссылочка:

.. csv-table:: Таблица, как таблица - не шо папало!!!
  :file: files/table123.csv
  :widths:  40, 7, 12, 41
  :header-rows: 1
  
продолжение следует!



Предшествует текст |армагедон| после этого все фильтры будут сброшены.

.. include:: files/12345.rst

Если хочешь добавить документ в документ: http://docutils.sourceforge.net/docs/ref/rst/directives.html#miscellaneous

wwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwwww

А теперь невероятный трюк:

.. include:: Captain.rst

Предполагаю, что далее может ничего без названия не отображаться:

.. include:: without_name.rst



