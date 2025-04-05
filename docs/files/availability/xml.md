# 📦 Структура XML-файла с остатками и ценами

XML-файл с остатками и ценами содержит информацию о наличии товаров на складах и их ценах.

## Общая структура

Файл представляет собой XML-документ со следующей структурой:

```xml
<?xml version="1.0" ?>
<root>
  <metainfo>
    <!-- Метаинформация о выгрузке -->
  </metainfo>
  <tires>
    <!-- Информация о наличии и ценах шин -->
  </tires>
  <wheels>
    <!-- Информация о наличии и ценах дисков -->
  </wheels>
</root>
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

```xml
<metainfo>
  <utc_update_time>2025-04-05 09:03:06.160749+00:00</utc_update_time>
  <client_name>mrnr</client_name>
  <license_expire>2025-04-05</license_expire>
</metainfo>
```

---

## Поля элементов раздела `tires`

Раздел `tires` содержит элементы с информацией о наличии и ценах шин. Каждый элемент `<item>` представляет одну позицию:

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

**Пример элемента `<item>` в разделе `tires`**:

```xml
<item>
  <code>t557858</code>
  <stock_name>4x4sport_vladivostok</stock_name>
  <stock_name_ru>4x4sport Владивосток</stock_name_ru>
  <wholesale_price>23000.00</wholesale_price>
  <quantity>10</quantity>
  <recommended_retail_price/>
  <minimal_internet_price/>
  <provider_key>ETL28398000</provider_key>
  <cae>ETL28398000</cae>
  <year/>
  <sale>false</sale>
  <price>23000</price>
  <delivery_time>0</delivery_time>
</item>
```

---

## Поля элементов раздела `wheels`

Раздел `wheels` содержит элементы с информацией о наличии и ценах дисков. Структура элементов идентична структуре элементов в разделе `tires`.


**Особенности XML формата**:
- Пустые значения для опциональных полей представлены пустыми тегами (например, `<recommended_retail_price/>`)
- Булевы значения представлены как текст: `true` или `false` 
