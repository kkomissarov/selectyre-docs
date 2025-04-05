# 📦 Структура JSON-файла с остатками и ценами

JSON-файл с остатками и ценами содержит информацию о наличии товаров на складах и их ценах.

## Общая структура

Файл представляет собой объект JSON, содержащий три основные секции:

```json
{
  "metainfo": { ... },
  "tires": [ ... ],
  "wheels": [ ... ]
}
```

---

## Поля раздела `metainfo`

Раздел `metainfo` содержит общую информацию о выгрузке:

| Поле              | Тип     | Описание                               |
|-------------------|---------|----------------------------------------|
| `utc_update_time` | string  | Дата и время формирования выгрузки в UTC |
| `client_name`     | string  | Имя клиента                           |
| `license_expire`  | string  | Дата истечения лицензии               |

**Пример секции `metainfo`**:

```json
"metainfo": {
  "utc_update_time": "2025-04-05T09:03:06.160Z",
  "client_name": "mrnr",
  "license_expire": "2025-04-05"
}
```

---

## Поля элементов раздела `tires`

Раздел `tires` содержит массив объектов с информацией о наличии и ценах шин:

| Поле                       | Тип          | Описание                               |
|----------------------------|--------------|----------------------------------------|
| `code`                     | string       | Уникальный код шины                    |
| `stock_name`               | string       | Идентификатор склада                   |
| `stock_name_ru`            | string       | Название склада (на русском)           |
| `wholesale_price`          | string       | Оптовая цена                           |
| `quantity`                 | integer      | Количество на складе                   |
| `recommended_retail_price` | string \| null | Рекомендованная розничная цена         |
| `minimal_internet_price`   | string \| null | Минимальная интернет-цена              |
| `provider_key`             | string       | Код поставщика                         |
| `cae`                      | string       | Код производителя                      |
| `year`                     | string \| null | Год производства                       |
| `sale`                     | boolean      | Распродажа (true/false)                |
| `price`                    | string       | Цена                                   |
| `delivery_time`            | integer      | Время доставки (в днях)                |

**Пример объекта в разделе `tires`**:

```json
{
  "code": "t557858",
  "stock_name": "4x4sport_vladivostok",
  "stock_name_ru": "4x4sport Владивосток",
  "wholesale_price": "23000.00",
  "quantity": 10,
  "recommended_retail_price": null,
  "minimal_internet_price": null,
  "provider_key": "ETL28398000",
  "cae": "ETL28398000",
  "year": null,
  "sale": false,
  "price": "23000",
  "delivery_time": 0
}
```

---

## Поля элементов раздела `wheels`

Раздел `wheels` содержит массив объектов с информацией о наличии и ценах дисков. Структура объектов идентична структуре объектов в разделе `tires`:
