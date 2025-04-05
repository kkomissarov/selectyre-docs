# 📦 Структура JSON-файла с товарами

## Общая структура

```json
{
  "metainfo": { ... },
  "tires": [ ... ],
  "wheels": [ ... ]
}
```

---

## 🧠 `metainfo` — Метаданные

Информация о клиенте и времени обновления данных.

| Поле               | Тип     | Описание                         |
|--------------------|---------|----------------------------------|
| `utc_update_time`  | string  | Время последнего обновления (UTC, ISO 8601) |
| `client_name`      | string  | Название клиента                 |
| `license_expire`   | string  | Срок действия лицензии |

📌 **Пример**:

```json
"metainfo": {
  "utc_update_time": "2025-04-01T19:20:20.861Z",
  "client_name": "mrnr",
  "license_expire": "2025-04-01"
}
```

---

## 🛞 `tires` — Шины

Массив объектов, описывающих шины.

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


📌 **Пример**:

```json
{
  "code": "t499551",
  "p_full_name": "Viatti Brina Nordico V-522 245/45 R17 95T",
  "p_brand": "Viatti",
  "p_model": "Brina Nordico V-522",
  "p_width": "245.00",
  "p_height": "45.00",
  "p_diameter": "17.00",
  "p_load_index": "95",
  "p_speed_index": "T",
  "p_season": "Зимняя",
  "p_category": "Легковые",
  "p_xl": false,
  "p_thorn": true,
  "p_can_thorn": false,
  "p_runflat": false
}
```

---

## 🛞 `wheels` — Диски

Массив объектов, описывающих колесные диски.

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

```json
{
  "code": "w446258",
  "p_full_name": "NZ SH675 6.5x16 5*105 ET39 DIA56.6 BKF Литой",
  "p_brand": "NZ",
  "p_model": "SH675",
  "p_color": "BKF",
  "p_human_readable_color": "Черный и комбинации",
  "p_width": "6.50",
  "p_diameter": "16.00",
  "p_bolts_count": 5,
  "p_bolts_space": "105",
  "p_pcd": "5x105",
  "p_et": "39.00",
  "p_dia": "56.60",
  "p_type": "Литой"
}
```
