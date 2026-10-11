# Sayohatlar

Aylanadigan 3D globus: borilgan davlat ustiga bosilsa, o‘sha yerda tushgan rasmlar ochiladi.

## Ishga tushirish

Sayt bitta sahifadan iborat, yig‘ish (build) kerak emas. `trips.json` faylini o‘qigani uchun uni
oddiy veb-server orqali oching:

```
python3 -m http.server 8000
```

So‘ng brauzerda `http://localhost:8000` manzilini oching. GitHub Pages’da ham shu holicha ishlaydi
(Settings → Pages → Branch: `main`, papka: `/root`).

## Davlat va rasm qo‘shish

1. Rasmni `photos/` papkasiga soling (JPG, uzun tomoni 1600 px atrofida bo‘lgani ma’qul).
2. `trips.json` ichidagi `places` ro‘yxatiga yozing:

```json
{"id": "FRA", "year": "2019", "note": "Qisqa xotira", "photos": [
  {"f": "photos/fra-01.jpg", "c": "Eyfel minorasi"}
]}
```

`id` — davlatning uch harfli ISO kodi (`TUR`, `USA`, `GBR` ...). Ro‘yxatdagi birinchi rasm globusdagi
belgining muqovasi bo‘ladi. `home` — parvoz yoylari boshlanadigan shahar.

## Fayllar

- `index.html` — butun sayt (globus, panel, qidiruv)
- `trips.json` — davlatlar, yillar, izohlar va rasmlar ro‘yxati
- `photos/` — rasmlar

Xarita va shriftlar CDN’dan yuklanadi (d3, datamaps, Google Fonts), shuning uchun internet kerak.
