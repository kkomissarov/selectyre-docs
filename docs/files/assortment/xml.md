# 📦 Структура XML-файла с товарами

XML-файл с ассортиментом товаров содержит информацию о шинах и дисках в формате XML.

📖 **Подробное описание всех полей см. в разделе [Структура данных](../data_structure.md)**

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

Раздел с общей информацией о выгрузке. Описание полей см. в [Структуре данных → Метаданные](../data_structure.md#метаданные-metainfo).

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

Набор элементов `item`, описывающих шины. Описание полей см. в [Структуре данных → Поля шин](../data_structure.md#поля-шин).

📌 **Пример элемента**:

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
    <p_photo>https://lk.selectyre.ru/photo-processor/get-photo/...</p_photo>
    <p_shipping_weight>11.60</p_shipping_weight>
    <p_shipping_volume>0.10</p_shipping_volume>
    <p_shipping_length>66.00</p_shipping_length>
    <p_shipping_width>66.00</p_shipping_width>
    <p_shipping_height>25.00</p_shipping_height>
  </item>
</tires>
```

---

## 🔘 `wheels` — Диски

Набор элементов `item`, описывающих колесные диски. Описание полей см. в [Структуре данных → Поля дисков](../data_structure.md#поля-дисков).

📌 **Пример элемента**:

```xml
<wheels>
  <item>
    <code>w446258</code>
    <p_full_name>NZ SH675 6.5x16 5*105 ET39 DIA56.6 BKF Литой</p_full_name>
    <p_brand>NZ</p_brand>
    <p_model>SH675</p_model>
    <p_category>Легковые</p_category>
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
    <p_photo>https://lk.selectyre.ru/photo-processor/get-photo/...</p_photo>
    <p_shipping_weight>10.00</p_shipping_weight>
    <p_shipping_volume>0.12</p_shipping_volume>
    <p_shipping_length>41.00</p_shipping_length>
    <p_shipping_width>41.00</p_shipping_width>
    <p_shipping_height>17.00</p_shipping_height>
  </item>
</wheels>
``` 