# 📦 Структура CSV-файла с остатками и ценами шин

CSV-файл с остатками и ценами шин представляет собой таблицу, где каждая строка содержит информацию о наличии и цене конкретной шины на определённом складе.

## Общая структура

```csv
code,stock_name,stock_name_ru,wholesale_price,quantity,recommended_retail_price,minimal_internet_price,provider_key,cae,year,sale,price,delivery_time
t499551,zapaska_novosibirsk,Запаска Новосибирск,10633.00,8,,12430.00,00000026791,3151028,,False,10633,0
...
```

Первая строка файла содержит заголовки столбцов, которые соответствуют названиям полей.

---

## Поля CSV-файла с остатками и ценами шин

Файл содержит следующие столбцы:

| Поле                       | Тип          | Описание                               |
|----------------------------|--------------|----------------------------------------|
| `code`                     | string       | Уникальный код шины                    |
| `stock_name`               | string       | Идентификатор склада                   |
| `stock_name_ru`            | string       | Название склада (на русском)           |
| `wholesale_price`          | string       | Оптовая цена                           |
| `quantity`                 | integer      | Количество на складе                   |
| `recommended_retail_price` | string       | Рекомендованная розничная цена         |
| `minimal_internet_price`   | string       | Минимальная интернет-цена              |
| `provider_key`             | string       | Код поставщика                         |
| `cae`                      | string       | Код производителя                      |
| `year`                     | string       | Год производства                       |
| `sale`                     | boolean      | Распродажа (True/False)                |
| `price`                    | string       | Цена                                   |
| `delivery_time`            | integer      | Время доставки (в днях)                |

## Особенности формата

1. Строки разделяются символом переноса строки (`\n`)
2. Столбцы разделяются запятыми (`,`)
3. Текстовые значения могут быть заключены в двойные кавычки (`"`)
4. Пустые значения для опциональных полей представлены пустой строкой
5. Булевы значения представлены как `True` или `False`

📌 **Пример строки данных**:

```csv
t499551,zapaska_novosibirsk,Запаска Новосибирск,10633.00,8,,12430.00,00000026791,3151028,,False,10633,0
```

# Структура CSV файла остатков и цен шин

Данный раздел находится в разработке.

В CSV файле с остатками и ценами содержится информация о доступности и стоимости шин.

## Поля

| Поле | Тип | Описание |
|------|-----|----------|
| `code` | строка | Уникальный код шины, соответствующий коду из файла ассортимента |
| `price` | число | Цена шины в рублях |
| `quantity` | число | Доступное количество |
| `in_stock` | булево | Флаг наличия на складе |
| ... | ... | ... |

Полная документация по структуре данного файла будет добавлена позднее.
