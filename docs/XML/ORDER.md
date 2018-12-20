
Заказ (ORDER) на поставку отправляет покупатель поставщику, указывая штрихкод продукта, его описание, заказанное количество, цену и прочую необходимую информацию.

| Поехали | Первый |    Второй     |     Сабака      | Кенгуру |
| ------- | ------ | ------------- | --------------- | ------- |
|         |        |      Парабола |     Клевер      |  Мишь   |
|         |        |    Кентавр    |           Лопух |         |
|         |        |               |                 |         |
|         |        |               |                 |         |









|**Название поля**|**Тип**|**Формат**|**Описание**
| :--- | :--- | :--- | :--- |
|**&lt;ORDER&gt;**| | |
|     &lt;DOCUMENTNAME&gt;&lt;/DOCUMENTNAME&gt;|М|Число положительное|Название документа (220 —заказ)
|     &lt;NUMBER&gt;&lt;/NUMBER&gt;|М|Строка (50)|Номер заказа
|     &lt;DATE&gt;&lt;/DATE&gt;|М|Дата (ГГГГ-ММ-ДД)|Дата документа
|     &lt;ACTION&gt;&lt;/ACTION&gt;|О|«4», «5», «27», «29»|4 — поставка изменена, 5 — замена документа, 29 — поставка принята, 27 — поставка не принята
|     &lt;VERSION&gt;&lt;/VERSION&gt;|O|Число положительное|Версия заказа
|     &lt;PROMO&gt;&lt;/PROMO&gt;|O|«0», «1»|Акция: 0 — нет, 1 — есть
|     &lt;DELIVERYDATE&gt;&lt;/DELIVERYDATE&gt;|М|Дата (ГГГГ-ММ-ДД)|Дата поставки
|     &lt;DELIVERYTIME&gt;&lt;/DELIVERYTIME&gt;|O|Время (чч:мм)|Время поставки
|     &lt;SHIPMENTDATE&gt;&lt;/SHIPMENTDATE&gt;|O|Дата (ГГГГ-ММ-ДД)|Дата отгрузки6
|     &lt;SHIPMENTTIME&gt;&lt;/SHIPMENTTIME&gt;|O|Время (чч:мм)|Время отгрузки
|     &lt;CAMPAIGNNUMBER&gt;&lt;/CAMPAIGNNUMBER&gt;|O|Строка (70)|Номер договора на поставку
|     &lt;CAMPAIGNNUMBERDATE&gt;&lt;/CAMPAIGNNUMBERDATE&gt;|O|Дата (ГГГГ-ММ-ДД)|Дата договора
|     &lt;CURRENCY&gt;&lt;/CURRENCY&gt;|O|Строка (3)|Код валюты
|     &lt;TRANSPORTQUANTITY&gt;&lt;/TRANSPORTQUANTITY&gt;|O|Число положительное|Количество машин
|     &lt;ORDERREFERENCENUMBER&gt;5&lt;/ORDERREFERENCENUMBER&gt;| |Строка (16)|Уникальный номер заказа для отслеживания
|     **&lt;LIMES&gt;**| | |Детали транспорта
|          &lt;LIMESNAME&gt;&lt;/LIMESNAME&gt;|O|Строка (70)|Название рампы
|          &lt;DATEFROM&gt;&lt;/DATEFROM&gt;|O|Дата (ГГГГ-ММ-ДД)|Дата прибытия транспорта
|          &lt;TIMEFROM&gt;&lt;/TIMEFROM&gt;|O|Время (чч:мм)|Время прибытия транспорта
|          &lt;DATETO&gt;&lt;/DATETO&gt;|O|Дата (ГГГГ-ММ-ДД)|Дата окончания отгрузки
|          &lt;TIMETO&gt;&lt;/TIMETO&gt;|O|Время (чч:мм)|Время окончания отгрузки
|     **&lt;/LIMES&gt;**| | |
|     &lt;VAT&gt;&lt;/VAT&gt;|O|Число положительное|Ставка НДС, %
|     &lt;TRANSPORTATIONTYPES&gt;&lt;/TRANSPORTATIONTYPES&gt;|O|Строка (35)|Вид транспортировки
|     &lt;TRANSPORTATIONMEANS&gt;&lt;/TRANSPORTATIONMEANS&gt;|O|Строка (70)|Транспортное средство
|     &lt;TRANSPORTATIONCONDITION&gt;&lt;/TRANSPORTATIONCONDITION&gt;|O|Строка (70)|Условия транспортировки
|     &lt;TRANSPORTATIONPAYMENTTYPE&gt;&lt;/TRANSPORTATIONPAYMENTTYPE&gt;|O|Строка (35)|Тип оплаты доставки
|     &lt;TRANSPORTATIONROUTE&gt;&lt;/TRANSPORTATIONROUTE&gt;|O|Строка (70)|Маршрут доставки
|     &lt;BLANKETORDERNUMBER&gt;&lt;/BLANKETORDERNUMBER&gt;|O|Строка (35)|Номер бланкового заказа
|     &lt;INFOCODED&gt;&lt;/INFOCODED&gt;|O|Строка (35)|Инфокод
|     &lt;DOCTYPE&gt;&lt;/DOCTYPE&gt;|O|Строка (1)|Тип документа: O — оригинал, R — замена, D — удаление, F — фиктивность заказа, PO — предзаказ
|     &lt;CORRNUMBER&gt;&lt;/CORRNUMBER&gt;| | |
|     &lt;SUPORDER&gt;&lt;/SUPORDER&gt;|O|Строка (35)|Номер заказа поставщика
|     &lt;KDKNUM&gt;&lt;/KDKNUM&gt;|O|Строка (35)|Номер общего заказа КДК
|     &lt;ORDRTYPE&gt;&lt;/ORDRTYPE&gt;|O|Строка (35)|Тип заказа
|     &lt;INFO&gt;&lt;/INFO&gt;|O|Строка (70)|Свободный текст
|     &lt;EARLIESTDELIVERYDATE&gt;&lt;/EARLIESTDELIVERYDATE&gt;|O|Дата (ГГГГ-ММ-ДД)|Дата не раньше
|     &lt;LATESTDELIVERYDATE&gt;&lt;/LATESTDELIVERYDATE&gt;|O|Дата (ГГГГ-ММ-ДД)|Дата не позднее
|     **&lt;HEAD&gt;**| | |
|          &lt;SUPPLIER&gt;&lt;/SUPPLIER&gt;|M|Число (13)|GLN поставщика
|          &lt;BUYER&gt;&lt;/BUYER&gt;|M|Число (13)|GLN покупателя
|          &lt;BUYERCODE&gt;&lt;/BUYERCODE&gt;|O|Строка (35)|Код покупателя
|          &lt;DELIVERYPLACE&gt;&lt;/DELIVERYPLACE&gt;|M|Число (13)|GLN места доставки
|          &lt;FINALRECIPIENT&gt;&lt;/FINALRECIPIENT&gt;|O|Число (13)|GLN конечного консигнатора
|          &lt;ORDERPARTNER&gt;&lt;/ORDERPARTNER&gt;|O|Число (13)|GLN заказчика
|          &lt;INVOICEPARTNER&gt;&lt;/INVOICEPARTNER&gt;|O|Число (13)|GLN плательщика
|          &lt;SENDER&gt;&lt;/SENDER&gt;|M|Число (13)|GLN отправителя сообщения
|          &lt;RECIPIENT&gt;&lt;/RECIPIENT&gt;|M|Число (13)|GLN получателя сообщения
|          &lt;CONSIGNEE&gt;&lt;/CONSIGNEE&gt;|О11|Число (13)|GLN грузополучателя
|          &lt;RECIPIENTCODE&gt;&lt;/RECIPIENTCODE&gt;|O|Строка (35)|Код получателя
|          &lt;RECIPIENTNAME&gt;&lt;/RECIPIENTNAME&gt;|O|Строка (70)|Имя получателя
|          &lt;INFO&gt;&lt;/INFO&gt;|O|Строка (70)|Свободный текст
|          &lt;DISCOUNTVALUE&gt;&lt;/DISCOUNTVALUE&gt;|O|Число положительное|Размер скидки
|          &lt;RECIPIENTCONTACTFACE&gt;&lt;/RECIPIENTCONTACTFACE&gt;|O|Строка (70)|Контактное лицо
|          &lt;RECIPIENTPHONE&gt;&lt;/RECIPIENTPHONE&gt;|O|Строка (35)|Телефон получателя
|          &lt;RECIPIENTCITY&gt;&lt;/RECIPIENTCITY&gt;|O|Строка (35)|Город получателя
|          &lt;RECIPIENTADRESS&gt;&lt;/RECIPIENTADRESS&gt;|O|Строка (70)|Адрес получателя
|          &lt;EDIINTERCHANGEID&gt;&lt;/EDIINTERCHANGEID&gt;|O|Строка (70)|Номер транзакции
|          **&lt;POSITION&gt;**| | |
|               &lt;POSITIONNUMBER&gt;&lt;/POSITIONNUMBER&gt;|М|Число положительное|Номер товарной позиции
|               &lt;PRODUCT&gt;&lt;/PRODUCT&gt;|M|Число (8, 10, 14)|Штрихкод продукта
|               &lt;PRODUCTIDSUPPLIER&gt;&lt;/PRODUCTIDSUPPLIER&gt;|O|Строка (16)|Артикул в БД
|               &lt;PRODUCTIDBUYER&gt;&lt;/PRODUCTIDBUYER&gt;|O|Строка (16)|Артикул в БД покупателя
|               &lt;BUYERPARTNUMBER&gt;&lt;/BUYERPARTNUMBER&gt;|О|Строка (16)|Внутренний системный номер артикула в БД покупателя
|               &lt;ORDEREDQUANTITY&gt;&lt;/ORDEREDQUANTITY&gt;|M|Число положительное|Заказанное количество
|               &lt;QUANTITYOFCUINTU&gt;&lt;/QUANTITYOFCUINTU&gt;|О|Число положительное|Количество в упаковке
|               &lt;ORDERUNIT&gt;&lt;/ORDERUNIT&gt;|О|Строка (3)|Единицы измерения (см. Приложение 3)ﾧ
|               &lt;QUANTITYOFPACKS&gt;&lt;/QUANTITYOFPACKS&gt;|О|Число положительное|Количество упаковок
|               &lt;ORDERPRICE&gt;&lt;/ORDERPRICE&gt;|O|Число десятичное|Цена продукта без НДС
|               &lt;PRICEWITHVAT&gt;&lt;/PRICEWITHVAT&gt;|O|Число десятичное|Цена продукта с НДС
|               &lt;AMOUNT&gt;&lt;/AMOUNT&gt;|O|Число десятичное|Сумма товара (без НДС)
|               &lt;AMOUNTWITHVAT&gt;&lt;/AMOUNTWITHVAT&gt;|О|Число десятичное|Сумма товара (с НДС)
|               &lt;VAT&gt;&lt;/VAT&gt;|O|Число десятичное|Ставка НДС, %
|               &lt;CLAIMEDDELIVERYDATE&gt;&lt;/CLAIMEDDELIVERYDATE&gt;|O|Дата (ГГГГ-ММ-ДД)|Объявленная дата доставки
|               &lt;CLAIMEDDELIVERYTIME&gt;&lt;/CLAIMEDDELIVERYTIME&gt;|O|Время (чч:мм)|Объявленное время доставки
|               &lt;DELIVERYPLACE&gt;&lt;/DELIVERYPLACE&gt;|О|Число (13)|GLN конечного места доставки
|               &lt;INFOCODED&gt;&lt;/INFOCODED&gt;|O|Строка (35)|Инфокод
|               &lt;MINIMUMORDERQUANTITY&gt;&lt;/MINIMUMORDERQUANTITY&gt;|O|Число положительное|Минимальное заказанное количество
|               &lt;MAXIMUMORDERQUANTITY&gt; &lt;/MAXIMUMORDERQUANTITY&gt;|O|Число положительное|Максимально допустимое отгрузжаемое количество
|               &lt;PRODUCTIONCODE&gt;&lt;/PRODUCTIONCODE&gt;|О|Строка (16)|Код алкогольной продукции
|               &lt;POSITIONKGM&gt;50&lt;/POSITIONKGM&gt;|М| |Всего килограмм по позиции
|               &lt;INFO&gt;&lt;/INFO&gt;|O|Строка (90)|Свободный текст
|               &lt;COMPAIGNNUMBER&gt;&lt;/COMPAIGNNUMBER&gt;|O|Строка (70)|Номер поставщика
|               &lt;EARLIESTDELIVERYDATE&gt;&lt;/EARLIESTDELIVERYDATE&gt;|O|Дата (ГГГГ-ММ-ДД)|Поставка не раньше указанной даты
|               &lt;LATESTDELIVERYDATE&gt;&lt;/LATESTDELIVERYDATE&gt;|O|Дата (ГГГГ-ММ-ДД)|Поставка не позднее указанной даты
|               &lt;LATESTDELIVERYTIME&gt;&lt;/LATESTDELIVERYTIME&gt;|O|Время (чч:мм)|Поставка не позднее указанного времени
|               &lt;CONDITIONSTATUS&gt;&lt;/CONDITIONSTATUS&gt;|О|Строка (3)|Статус кондиции (см. Приложение 2)ﾧ
|               &lt;PACKAGEID&gt;&lt;/PACKAGEID&gt;|O|Число положительное|Идентификатор упаковки
|               &lt;CATEGORYNAME&gt;&lt;/CATEGORYNAME&gt;|O|Строка (70)|Наименование категории товара
|               &lt;BRENDNAME&gt;&lt;/BRENDNAME&gt;|O|Строка (70)|Наименование бренда
|               &lt;GROUPNAME&gt;ведро 9.6кг&lt;/GROUPNAME&gt;| | |Наименование группы товара
|               &lt;NOVELTY&gt;&lt;/NOVELTY&gt;|O| |Новинка
|               &lt;COUNTPIECESINBOX&gt;&lt;/COUNTPIECESINBOX&gt;|O|Число положительное|Количество частей в упаковке
|               &lt;COUNTBOXESINLAYER&gt;&lt;/COUNTBOXESINLAYER&gt;|O|Число положительное|Количество упаковок на уровне
|               &lt;COUNTPERPALLET&gt;&lt;/COUNTPERPALLET&gt;|O|Число положительное|Количество на паллете
|               &lt;WEIGHT&gt;&lt;/WEIGHT&gt;|O|Число десятичное|Вес
|               &lt;PALLETS&gt;&lt;/PALLETS&gt;|O|Число положительное|Количество паллет
|               &lt;COUNTRYORIGIN&gt;&lt;/COUNTRYORIGIN&gt;|О|Строка (2)|Страна производитель
|               &lt;CALIBRE&gt;&lt;/CALIBRE&gt;|O|Число положительное|Диаметр
|               &lt;PRICEWITHDISCOUNT&gt;&lt;/PRICEWITHDISCOUNT&gt;|O|Число десятичное|Цена с учетом скидки
|               &lt;BOXESCOUNT&gt;&lt;/BOXESCOUNT&gt;|O|Число положительное|Количество упаковок
|               **&lt;CHARACTERISTIC&gt;**| | |
|                    &lt;DESCRIPTION&gt;&lt;/DESCRIPTION&gt;|О|Строка (70)|Описание продукта
|               **&lt;/CHARACTERISTIC&gt;**| | |
|               **&lt;PACKING&gt;**| | |
|                    &lt;PACKINGTYPE&gt;&lt;/PACKINGTYPE&gt;|O|Строка (3)|Тип упаковки
|                    &lt;PACKINGQUANTITY&gt;&lt;/PACKINGQUANTITY&gt;|O|Число положительное|Количество упаковок
|                    &lt;PACKINGUNIT&gt;&lt;/PACKINGUNIT&gt;|O|Число положительное|Упаковщик
|               **&lt;/PACKING&gt;**| | |
|          **&lt;/POSITION&gt;**| | |
|     **&lt;/HEAD&gt;**| | |
|**&lt;ORDER&gt;**| | |


