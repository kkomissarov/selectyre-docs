# 📦 Структура CSV-файла с шинами

CSV-файл с ассортиментом шин представляет собой таблицу, где каждая строка содержит информацию об одной модели шины, а столбцы содержат различные характеристики.

## Общая структура

```csv
code,p_full_name,p_brand,p_model,...
t499551,Viatti Brina Nordico V-522 245/45 R17 95T,Viatti,Brina Nordico V-522,...
...
```

Первая строка файла содержит заголовки столбцов, которые соответствуют названиям полей.

---

## Поля CSV-файла с шинами

Файл содержит следующие столбцы:

| Поле                | Тип      | Описание                                  |
|---------------------|----------|-------------------------------------------|
| `code`              | string   | Уникальный код шины                       |
| `p_full_name`       | string   | Полное наименование                       |
| `p_brand`           | string   | Бренд                                     |
| `p_model`           | string   | Модель                                    |
| `p_width`           | string   | Ширина профиля в мм                       |
| `p_height`          | string   | Профиль (высота в % от ширины)            |
| `p_diameter`        | string   | Диаметр в дюймах                          |
| `p_load_index`      | string   | Индекс нагрузки                           |
| `p_speed_index`     | string   | Индекс скорости                           |
| `p_season`          | string   | Сезонность (например, "Зимняя", "Летняя") |
| `p_category`        | string   | Категория (например, "Легковые")          |
| `p_xl`              | boolean  | Усиленная шина (Extra Load)               |
| `p_protection`      | string \| null | Защита обода                              |
| `p_mud_terrain`     | boolean  | Грязевая шина                             |
| `p_all_terrain`     | boolean  | Вседорожная                               |
| `p_cargo`           | boolean  | Грузовая                                  |
| `p_thorn`           | boolean  | С шипами                                  |
| `p_can_thorn`       | boolean  | Возможна ошиповка                         |
| `p_omologation`     | string \| null | Омологация                                |
| `p_side`            | string \| null | Надпись на боковине                       |
| `p_runflat`         | boolean  | RunFlat шина                              |
| `p_axis`            | string \| null | Ось установки                             |
| `p_layering`        | string \| null | Слойность                                 |
| `p_appointment`     | string \| null | Назначение                                |
| `p_photo`           | string   | Ссылка на фото                            |
| `p_photo_last_modified` | string | Дата последнего обновления фото           |
| `p_info_last_modified`  | string | Дата последнего обновления информации     |
| `p_shipping_weight`     | string | Вес при отгрузке, кг                      |
| `p_shipping_volume`     | string | Объем при отгрузке, м³                    |
| `p_shipping_length`     | string | Длина упаковки, см                        |
| `p_shipping_width`      | string | Ширина упаковки, см                       |
| `p_shipping_height`     | string | Высота упаковки, см                       |

> Ссылки из параметра p_photo возвращают изображение с наложенным логотипом клиента. 
> Для того, чтобы они работали, нужно предоставить логотип администатору сервиса. 
> Если логотип не предоставлен, ссылки будут возвращать ошибку 404.

## Особенности формата

1. Строки разделяются символом переноса строки (`\n`)
2. Столбцы разделяются запятыми (`,`)
3. Текстовые значения могут быть заключены в двойные кавычки (`"`)
4. Пустые значения для опциональных полей представлены пустой строкой
5. Булевы значения представлены как `True` или `False`

📌 **Пример строки данных**:

```csv
t499551,Viatti Brina Nordico V-522 245/45 R17 95T,Viatti,Brina Nordico V-522,245.00,45.00,17.00,95,T,Зимняя,Легковые,False,,False,False,False,True,False,,,False,,,,2024-11-22 12:00:00.434530+00:00,2025-04-05 06:24:49.221270+00:00,https://lk.selectyre.ru/photo-processor/get-photo/eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJjb2RlIjoidDQ5OTU1MSJ9.u8pvAcFql6eyxxRPlYpqZAHQeD7kUuqv_wiSDtxJ7D8/,11.60,0.10,66.00,66.00,25.00
``` 