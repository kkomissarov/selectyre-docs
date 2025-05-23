# 📦 Структура XML-файла с товарами

## Общая структура

```xml
<?xml version="1.0" ?>
<root>
  <metainfo>...</metainfo>
  <tires>...</tires>
  <wheels>...</wheels>
</root>
```

---

## 🧠 `metainfo` — Метаданные

Информация о клиенте и времени обновления данных.

| Поле               | Тип     | Описание                         |
|--------------------|---------|----------------------------------|
| `utc_update_time`  | string  | Время последнего обновления (UTC) |
| `client_name`      | string  | Название клиента                 |
| `license_expire`   | string  | Срок действия лицензии |

📌 **Пример**:

```xml
<metainfo>
  <utc_update_time>2025-04-03 17:45:09.047607+00:00</utc_update_time>
  <client_name>mrnr</client_name>
  <license_expire>endless</license_expire>
</metainfo>
```

---

## 🛞 `tires` — Шины

Набор элементов `item`, описывающих шины.

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
> Для того чтобы они работали, нужно предоставить логотип администатору сервиса в формате jpeg или png. 
> Если логотип не предоставлен, ссылки будут возвращать ошибку 404.


📌 **Пример**:

```xml
<tires>
  <item>
    <code>t499551</code>
    <p_full_name>Viatti Brina Nordico V-522 245/45 R17 95T</p_full_name>
    <p_brand>Viatti</p_brand>
    <p_model>Brina Nordico V-522</p_model>
    <p_width>245.00</p_width>
    <p_height>45.00</p_height>
    <p_diameter>17.00</p_diameter>
    <p_load_index>95</p_load_index>
    <p_speed_index>T</p_speed_index>
    <p_season>Зимняя</p_season>
    <p_category>Легковые</p_category>
    <p_xl>false</p_xl>
    <p_protection/>
    <p_mud_terrain>false</p_mud_terrain>
    <p_all_terrain>false</p_all_terrain>
    <p_cargo>false</p_cargo>
    <p_thorn>true</p_thorn>
    <p_can_thorn>false</p_can_thorn>
    <p_omologation/>
    <p_side/>
    <p_runflat>false</p_runflat>
    <p_axis/>
    <p_layering/>
    <p_appointment/>
    <p_photo_last_modified>2024-11-22 12:00:00.434530+00:00</p_photo_last_modified>
    <p_info_last_modified>2025-04-03 15:01:23.735472+00:00</p_info_last_modified>
    <p_photo>https://lk.selectyre.ru/photo-processor/get-photo/eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJjb2RlIjoidDQ5OTU1MSJ9.u8pvAcFql6eyxxRPlYpqZAHQeD7kUuqv_wiSDtxJ7D8/</p_photo>
    <p_shipping_weight>11.60</p_shipping_weight>
    <p_shipping_volume>0.10</p_shipping_volume>
    <p_shipping_length>66.00</p_shipping_length>
    <p_shipping_width>66.00</p_shipping_width>
    <p_shipping_height>25.00</p_shipping_height>
  </item>
</tires>
```

---

## 🛞 `wheels` — Диски

Набор элементов `item`, описывающих колесные диски.

| Поле                | Тип      | Описание |
|---------------------|----------|----------|
| `code`              | string   | Уникальный код диска |
| `p_full_name`       | string   | Полное наименование |
| `p_brand`           | string   | Производитель |
| `p_model`           | string   | Модель |
| `p_color`           | string   | Код цвета |
| `p_human_readable_color` | string | Человекочитаемый цвет |
| `p_width`           | string   | Ширина, дюймы |
| `p_diameter`        | string   | Диаметр, дюймы |
| `p_bolts_count`     | int      | Количество отверстий |
| `p_bolts_space`     | string   | Расстояние между болтами, мм |
| `p_pcd`             | string   | Сверловка (например, `5x105`) |
| `p_et`              | string   | Вылет (ET), мм |
| `p_dia`             | string   | Диаметр центрального отверстия (DIA), мм |
| `p_type`            | string   | Тип диска (например, "Литой") |
| `p_photo`           | string   | Ссылка на фото |
| `p_photo_last_modified` | string | Последнее обновление фото |
| `p_info_last_modified`  | string | Последнее обновление информации |
| `p_shipping_weight`     | string | Вес упаковки, кг |
| `p_shipping_volume`     | string | Объем упаковки, м³ |
| `p_shipping_length`     | string | Длина упаковки, см |
| `p_shipping_width`      | string | Ширина упаковки, см |
| `p_shipping_height`     | string | Высота упаковки, см |

📌 **Пример**:

```xml
<wheels>
  <item>
    <code>w446258</code>
    <p_full_name>NZ SH675 6.5x16 5*105 ET39 DIA56.6 BKF Литой</p_full_name>
    <p_brand>NZ</p_brand>
    <p_model>SH675</p_model>
    <p_color>BKF</p_color>
    <p_human_readable_color>Черный и комбинации</p_human_readable_color>
    <p_width>6.50</p_width>
    <p_diameter>16.00</p_diameter>
    <p_bolts_count>5</p_bolts_count>
    <p_bolts_space>105</p_bolts_space>
    <p_pcd>5x105</p_pcd>
    <p_et>39.00</p_et>
    <p_dia>56.60</p_dia>
    <p_type>Литой</p_type>
    <p_photo_last_modified>2023-07-24 07:34:13.695348+00:00</p_photo_last_modified>
    <p_info_last_modified>2025-04-03 15:09:01.498062+00:00</p_info_last_modified>
    <p_photo>https://lk.selectyre.ru/photo-processor/get-photo/eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyX2lkIjoxLCJjb2RlIjoidzQ0NjI1OCJ9.DEreivROUGnmgTRdIESVo6TBx-f4Xnvo-Zdgtx57l38/</p_photo>
    <p_shipping_weight>10.00</p_shipping_weight>
    <p_shipping_volume>0.12</p_shipping_volume>
    <p_shipping_length>41.00</p_shipping_length>
    <p_shipping_width>41.00</p_shipping_width>
    <p_shipping_height>17.00</p_shipping_height>
  </item>
</wheels>
``` 