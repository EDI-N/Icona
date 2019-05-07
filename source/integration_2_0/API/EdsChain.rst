######################################################################
Получение конкретной цепочки документов
######################################################################

Для работы с этим методом пользователь должен быть `авторизированным <https://ссылка на авторизацию>`__ .

С помощью метода **api/eds/chain** и задаваемых параметров получить (выгрузить) необходимые данные конкретной цепочки документов.

+-------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
|                      **Метод запроса**                      |                                                                                                  **HTTP GET**                                                                                                   |
+=============================================================+=================================================================================================================================================================================================================+
| **Content-Type**                                            | application/json (тело запроса/ответа в json формате в теле HTTP запроса                                                                                                                                        |
+-------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **URL запроса**                                             | https://edo-v2.edi-n.com/api/eds/chain?gln=9864065702429&chain_uuid=9fe45d32-35c7-44d0-9131-7257fc0c0f39&load_docs=true&load_bodies=true&load_package=true&load_comments=true&load_tags=true&load_statuses=true |
+-------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| **Параметры, передаваемые в URL (вместе с адресом метода)** | В строке заголовка (Header) "Set-Cookie" обязательно передается **SID** - токен полученный при авторизации                                                                                                      |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **Обязательные url-параметры:**                                                                                                                                                                                 |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **gln** - строка(13); номер GLN организации, которая связана с авторизированным пользователем платформы EDIN 2.0 на уровне аккаунта                                                                             |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **chain_uuid** - строка; ID цепочки                                                                                                                                                                             |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **Опциональные url-параметры (boolean фильтры):**                                                                                                                                                               |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **load_docs** - загружать ли документы относящиеся к цепочке                                                                                                                                                    |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **load_bodies** - загружать ли тела документов                                                                                                                                                                  |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **load_package** - загружать ли пакеты                                                                                                                                                                          |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **load_comments** - загружать ли комментарии                                                                                                                                                                    |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **load_tags** - загружать ли теги к документам                                                                                                                                                                  |
|                                                             |                                                                                                                                                                                                                 |
|                                                             | **load_statuses** - загружать ли статусы к документам                                                                                                                                                           |
+-------------------------------------------------------------+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+

.. hint:: Также возможно выполнить запрос в виде curl-строки:
          
          curl -X GET 'https://edo-v2.edi-n.com/api/eds/chain?gln=9864065702429&chain_uuid=9fe45d32-35c7-44d0-9131-7257fc0c0f39&load_docs=true&load_bodies=true&load_package=true&load_comments=true&load_tags=true&load_statuses=true' -b 'SID=458a0d38-5b56-4b8e-8998-009a1edd31eb'

Спецификация для расшифровки ключей curl запроса: https://curl.haxx.se/docs/manpage.html

--------------

**JSON-параметры в теле HTTP запроса/ответа**

--------------

**REQUEST**

--------------

В этом методе json-тело **запроса** отсутствует (другие данные передавать не нужно).

--------------

**RESPONSE**

--------------

Таблица 4 - Описание json-параметров, которые могут передаваться в **ответ** на метод API

.. csv-table:: 
  :file: for_csv/XChain.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 1

Таблица 5 - Описание параметров объекта **XChainStatus**)

.. csv-table:: 
  :file: for_csv/XChainStatus.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 1

Таблица 6 - Описание параметров объекта **XDocStatus**)

.. csv-table:: 
  :file: for_csv/XDocStatus.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 7 - Описание параметров объекта **XDoc**)

.. csv-table:: 
  :file: for_csv/XDoc.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 8 - Описание параметров объекта **XTag**)

.. csv-table:: 
  :file: for_csv/XTag.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 9 - Описание параметров объекта **XStatus**)

.. csv-table:: 
  :file: for_csv/XStatus.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 10 - Описание параметров объекта **XDocSignInfo**)

.. csv-table:: 
  :file: for_csv/XDocSignInfo.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 11 - Описание параметров объекта **XDocCommentsList**)

.. csv-table:: 
  :file: for_csv/XDocCommentsList.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 12 - Описание параметров объекта **XDocComment**)

.. csv-table:: 
  :file: for_csv/XDocComment.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 13 - Описание параметров объекта **XDocAttachment**)

.. csv-table:: 
  :file: for_csv/XDocAttachment.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 14 - Описание параметров объекта **XDocBodyForms**)

.. csv-table:: 
  :file: for_csv/XDocBodyForms.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 15 - Описание параметров объекта **XDocBody**)

.. csv-table:: 
  :file: for_csv/XDocBody.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 16 - Описание параметров объекта **XDocBodyType**)

.. csv-table:: 
  :file: for_csv/XDocBodyType.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0

Таблица 17 - Описание параметров объекта **XDocType**)

.. csv-table:: 
  :file: for_csv/XDocType.csv
  :widths:  1, 7, 12, 41
  :header-rows: 1
  :stub-columns: 0

.. _подробнее:

Таблица 18 - Описание **DocStatus** параметров (объект XDocStatus_)

.. csv-table:: 
  :file: for_csv/xdocstatus_p.csv
  :widths:  1, 60
  :header-rows: 1
  :stub-columns: 0

.. _описание_параметров:

Таблица 19 - Описание **DocType** параметров (объект XDocType_)

.. csv-table:: 
  :file: for_csv/xdoctype_p.csv
  :widths:  1, 19, 41
  :header-rows: 1
  :stub-columns: 0


--------------

**Примеры**

--------------

**Запрос не содержит тела (json)**

**Примеры url-запросов:**

- Получить перечень документов по определенной цепочке без загрузки их тел, пакетов, комментариев, тегов и статусов: ``https://edo-v2.edi-n.com/api/eds/chain?gln=9864232304302&chain_uuid=0fe60377-51db-4b7a-b7eb-cdf5fa91a46a&load_docs=true&load_bodies=false&load_package=false&load_comments=false&load_tags=false&load_statuses=false``


--------------

**Пример тела ответа (json):**

.. code:: ruby

    {
  "id": 1005,
  "uuid": "73ee333d-ca3d-4c93-97fa-0b75d58b0ff3",
  "packageID": 0,
  "type": {
    "type": 5,
    "title": "ordrsp",
    "description": "Подтверждение заказа"
  },
  "docsCount": 6,
  "lastInDocID": 1005,
  "lastOutDocID": 1055,
  "partnerId": 9,
  "important": false,
  "status": {
    "status": 2,
    "title": "sent"
  },
  "visualStatus": 0,
  "archive": false,
  "childs": [
    {
      "body": {
        "forms": {}
      },
      "attachments": [],
      "comments": [],
      "doc_id": 1005,
      "doc_uuid": "97c06d02-7c3c-4467-aaac-4a808078609f",
      "uuidSender": "4820128010004",
      "uuidReceiver": "9864065702429",
      "docNumber": "6422722fb78c4509b06eac43758e1545",
      "dateCreated": 1549025901,
      "dateChanged": 1549025901,
      "dateRead": 0,
      "docDate": 1550181600,
      "chain_id": 1005,
      "chain_uuid": "73ee333d-ca3d-4c93-97fa-0b75d58b0ff3",
      "family": 1,
      "hash": "A1E7FAD0A57C43C3200DFF024AD4124F",
      "type": {
        "type": 2,
        "title": "orders",
        "description": "Заказ"
      },
      "status": {
        "status": 4,
        "title": "inbox"
      },
      "exchange_status": "000000000000000000000000",
      "is_archive": false,
      "extraFields": {
        "buyer_uuid": "4820128010004",
        "doc_num": "6422722fb78c4509b06eac43758e1545",
        "order_number": "6422722fb78c4509b06eac43758e1545",
        "ftpex_file_date": "1549025900",
        "supplier_uuid": "9864065702429",
        "delivery_place_uuid": "4820128019007",
        "order_date": "1550181600",
        "delivery_date": "1551477600",
        "ftpex_file_name": "highload_orders_test.xml",
        "contract_number": "334455",
        "sender": "4820128010004",
        "doc_date": "1550181600",
        "recipient": "9864065702429",
        "action": "0"
      },
      "tags": [],
      "statuses": [],
      "multiExtraFields": {}
    },
    ...
    {
      "body": {
        "forms": {}
      },
      "attachments": [],
      "comments": [],
      "doc_id": 1055,
      "doc_uuid": "8c956e06-d681-4389-868e-ab27e587b3bb",
      "uuidSender": "9864065702429",
      "uuidReceiver": "4820128010004",
      "docNumber": "6422722fb78c4509b06eac43758e1545",
      "dateCreated": 1555406695,
      "dateChanged": 1555407136,
      "dateRead": 0,
      "docDate": 1550188800,
      "chain_id": 1005,
      "chain_uuid": "73ee333d-ca3d-4c93-97fa-0b75d58b0ff3",
      "family": 1,
      "hash": "765B2DEFE72AEA34CA4A8507E473E76F",
      "type": {
        "type": 5,
        "title": "ordrsp",
        "description": "Подтверждение заказа"
      },
      "status": {
        "status": 2,
        "title": "sent"
      },
      "exchange_status": "000000000000000000000000",
      "is_archive": false,
      "extraFields": {
        "order_date": "1550181600",
        "delivery_date": "1551477600",
        "contract_number": "334455",
        "sender": "4820128010004",
        "buyer_uuid": "4820128010004",
        "doc_num": "6422722fb78c4509b06eac43758e1545",
        "order_number": "6422722fb78c4509b06eac43758e1545",
        "doc_date": "1550188800",
        "action": "29",
        "supplier_uuid": "9864065702429",
        "delivery_place_uuid": "4820128019007"
      },
      "tags": [],
      "statuses": [],
      "multiExtraFields": {}
    }
  ],
  "hash": "48800BFDDF4C38598D723A42F0384F03"
  } 




