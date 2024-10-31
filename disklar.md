# CMD yordamida Disklarni Boshqarish – Diskka oid buyruqlar bo'yicha qo'llanma

Ushbu qo'llanma CMD yordamida Windows operatsion tizimida disklarni boshqarish bo'yicha aniq ko'rsatmalar beradi. Bu yerda siz DiskPart bilan bajariladigan vazifalarni CMD orqali qanday bajarishni o'rganasiz. Qo'llanma disk bo'limlarini boshqarish, diskni formatlash va disk ma'lumotlarini olish kabi operatsiyalarni o'z ichiga oladi.

## Mundarija

1. [Kirish](#kirish)
2. [Talablar](#talablar)
3. [Disk ma'lumotlarini ko'rish](#disk-ma'lumotlarini-ko'rish)
4. [Disklarni tanlash va boshqarish](#disklarni-tanlash-va-boshqarish)
5. [Bo'limlar yaratish va formatlash](#bo'limlar-yaratish-va-formatlash)
6. [Bo'lim hajmini o'zgartirish](#bo'lim-hajmini-o'zgartirish)
7. [Diskni tozalash](#diskni-tozalash)
8. [Eng yaxshi amaliyotlar va ogohlantirishlar](#eng-yaxshi-amaliyotlar-va-ogohlantirishlar)

---

### 1. Kirish

CMD yordamida disklarni boshqarish qudratli imkoniyatlarni taklif etadi, xuddi DiskPart kabi. Bu qo'llanma CMD buyruqlari orqali disklarni boshqarish va bo'limlashning asosiy amaliyotlarini ko'rib chiqadi. 

### 2. Talablar

Jarayonni boshlashdan oldin:
- CMD ni **Administrator** sifatida ishga tushiring.
- **Ma'lumotlaringizni zaxiralang**, ba'zi operatsiyalar qaytarib bo'lmasdir.

### 3. Disk ma'lumotlarini ko'rish

Disk ma'lumotlarini ko'rish uchun quyidagi buyruqlarni ishlatib, disk turi, hajmi va bo'lim ma'lumotlarini olishingiz mumkin.

#### Disklar ro'yxatini olish

```bash
wmic diskdrive list brief
```
Ushbu buyruq barcha mavjud disklar haqida qisqacha ma'lumot beradi.

Batafsil ma'lumot olish
Model, seriya raqami va holat haqida batafsil ma'lumot olish uchun:
```bash
wmic diskdrive get model,name,size,serialnumber,status
```
### 4. Disklarni tanlash va boshqarish
Muayyan diskni boshqarish uchun DiskPart yordamida quyidagi buyruqlardan foydalaning.
So‘ngra DiskPart dasturida disklarni ro‘yxatlash uchun:

Disklar ro'yxatini olish (**DiskPart** orqali)
```bash
diskpart
```
So‘ngra DiskPart dasturida disklarni ro‘yxatlash uchun:
```bash
list disk
```
Diskni tanlash
Kerakli diskni aniqlaganingizdan so‘ng, uni tanlash uchun:
```bash
select disk <disk_raqami>
```
### 5. Bo'limlar yaratish va formatlash
Yangi bo'lim yaratishingiz yoki mavjud bo'limlarni formatlashingiz mumkin.

Asosiy bo'lim yaratish
Disk tanlangandan so‘ng:
```bash
create partition primary
```
Bo'limni formatlash
Bo'limni NTFS formatida formatlash uchun:
```bash
format fs=ntfs quick
```
Agar FAT32 kerak bo'lsa, **ntfs** o'rniga **fat32** yozing.
### 6. Bo'lim hajmini o'zgartirish
CMD yordamida bo'lim hajmini kengaytirish yoki qisqartirish mumkin.

Bo'limni kengaytirish
Tanlangan bo'limni (bo'sh joy mavjud bo'lsa) kengaytirish uchun:
```bash
extend size=<MBdagi_hajm>
```
Bo'limni qisqartirish
Bo'lim hajmini kamaytirish uchun:
```bash
shrink desired=<MBdagi_hajm>
```
### 7. Diskni tozalash
Diskni tozalash barcha bo‘limlar va ma’lumotlarni o‘chiradi, natijada bo‘sh disk qoladi.

Tozalash buyrug'i
Kerakli diskni tanlagandan so'ng:
```bash
clean
```
To‘liq tozalash (To‘liq o‘chirish)
Diskni to‘liq tozalash uchun:
```bash
clean all
```
⚠️ Ogohlantirish: Ushbu buyruqni bekor qilishning imkoni yo'q. Juda ehtiyot bo'ling.

### 8. Eng yaxshi amaliyotlar va ogohlantirishlar
- Buyruqlarni bajarishdan oldin disk raqamlarini diqqat bilan tekshiring.
- Operatsiyalarni bajarishdan oldin ma'lumotlarni zaxiralang.
- **clean all** buyrug‘idan faqat kerak bo‘lganda foydalaning.


