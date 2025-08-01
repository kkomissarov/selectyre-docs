# 📦 Структура JSON-файла с товарами

JSON-файл с ассортиментом товаров содержит информацию о шинах и дисках в формате JSON.

📖 **Подробное описание всех полей см. в разделе [Структура данных](../data_structure.md)**

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

Раздел с общей информацией о выгрузке. Описание полей см. в [Структуре данных → Метаданные](../data_structure.md#метаданные-metainfo).

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

Массив объектов, описывающих шины. Описание полей см. в [Структуре данных → Поля шин](../data_structure.md#поля-шин).

📌 **Пример элемента массива**:

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
  "p_protection": null,
  "p_mud_terrain": false,
  "p_all_terrain": false,
  "p_cargo": false,
  "p_thorn": true,
  "p_can_thorn": false,
  "p_omologation": null,
  "p_side": null,
  "p_runflat": false,
  "p_axis": null,
  "p_layering": null,
  "p_appointment": null,
  "p_photo": "https://lk.selectyre.ru/photo-processor/get-photo/...",
  "p_photo_last_modified": "2024-11-22 12:00:00.434530+00:00",
  "p_info_last_modified": "2025-04-05 06:24:49.221270+00:00",
  "p_shipping_weight": "11.60",
  "p_shipping_volume": "0.10",
  "p_shipping_length": "66.00",
  "p_shipping_width": "66.00",
  "p_shipping_height": "25.00"
}
```

---

## 🔘 `wheels` — Диски

Массив объектов, описывающих колесные диски. Описание полей см. в [Структуре данных → Поля дисков](../data_structure.md#поля-дисков).

📌 **Пример элемента массива**:

```json
{
  "code": "w446258",
  "p_full_name": "NZ SH675 6.5x16 5*105 ET39 DIA56.6 BKF Литой",
  "p_brand": "NZ",
  "p_model": "SH675",
  "p_category": "Легковые",
  "p_color": "BKF",
  "p_human_readable_color": "Черный и комбинации",
  "p_width": "6.50",
  "p_diameter": "16.00",
  "p_bolts_count": 5,
  "p_bolts_space": "105",
  "p_pcd": "5x105",
  "p_et": "39.00",
  "p_dia": "56.60",
  "p_type": "Литой",
  "p_photo": "https://lk.selectyre.ru/photo-processor/get-photo/...",
  "p_photo_last_modified": "2023-07-24 07:34:13.695348+00:00",
  "p_info_last_modified": "2025-04-03 15:09:01.498062+00:00",
  "p_shipping_weight": "10.00",
  "p_shipping_volume": "0.12",
  "p_shipping_length": "41.00",
  "p_shipping_width": "41.00",
  "p_shipping_height": "17.00"
}
```
