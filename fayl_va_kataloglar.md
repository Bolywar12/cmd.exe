# Fayl va Kataloglar Bilan Ishlash – CMD Qo'llanma

Bu qo'llanma sizga Windows CMD (Command Prompt) yordamida fayl va kataloglar (papkalar) bilan ishlash bo'yicha asosiy va kengaytirilgan ko'nikmalarni o'rganishga yordam beradi. Bu yerda fayllarni yaratish, o'chirish, ko'chirish, nusxalash va kataloglarni boshqarish bilan bog'liq buyruqlarni topasiz.

## Mundarija

1. [Asosiy Buyruqlar](#asosiy-buyruqlar)
2. [Fayllarni Boshqarish](#fayllarni-boshqarish)
   - [Fayl Yaratish](#fayl-yaratish)
   - [Faylni O‘chirish](#faylni-o‘chirish)
   - [Faylni Ko‘chirish va Nusxalash](#faylni-ko‘chirish-va-nusxalash)
3. [Kataloglar Bilan Ishlash](#kataloglar-bilan-ishlash)
   - [Yangi Katalog Yaratish](#yangi-katalog-yaratish)
   - [Katalogga Kirish va Undan Chiqish](#katalogga-kirish-va-undan-chiqish)
   - [Katalogni O‘chirish](#katalogni-o‘chirish)
4. [Qo‘shimcha Kengaytirilgan Buyruqlar](#qo‘shimcha-kengaytirilgan-buyruqlar)
5. [Maslahat va Eng Yaxshi Amaliyotlar](#maslahat-va-eng-yaxshi-amaliyotlar)

---

### 1. Asosiy Buyruqlar

Bu bo‘limda CMD yordamida fayl va kataloglarni boshqarish uchun ishlatiladigan asosiy buyruqlarni o‘rganamiz. 

- **`dir`** – Katalogdagi fayl va papkalarni ro‘yxatlash.
- **`cd`** – Kataloglar orasida harakatlanish.
- **`mkdir`** – Yangi katalog yaratish.
- **`del`** – Fayl yoki fayllarni o‘chirish.
- **`copy`** – Fayllarni nusxalash.
- **`move`** – Fayllarni bir katalogdan boshqasiga ko‘chirish.

### 2. Fayllarni Boshqarish

#### Fayl Yaratish

CMD da yangi matnli fayl yaratish uchun quyidagi buyruqni ishlatish mumkin:

```cmd
echo Bu fayl CMD yordamida yaratildi > yangi_fayl.txt
```
Yuqoridagi buyruq "yangi_fayl.txt" faylini yaratadi va uning ichiga "Bu fayl CMD yordamida yaratildi" matnini yozadi.

Faylni O‘chirish
Keraksiz fayllarni o‘chirish uchun **`del`** buyrug‘idan foydalaniladi:
```cmd
del yangi_fayl.txt
```
⚠️Ogohlantirish: Bu buyruqni ehtiyotkorlik bilan ishlating, chunki o‘chirilgan fayllar qayta tiklanmaydi.

Faylni Ko‘chirish va Nusxalash
Faylni boshqa katalogga ko‘chirish yoki nusxalash:

 - Nusxalash uchun **`copy`** buyrug‘i ishlatiladi:
```cmd
copy yangi_fayl.txt C:\yangi_katalog\
```
 - Ko‘chirish uchun **`move`** buyrug‘i ishlatiladi:
```cmd
move yangi_fayl.txt C:\yangi_katalog\
```
### 3. Kataloglar Bilan Ishlash
Yangi Katalog Yaratish
Yangi katalog yaratish uchun **`mkdir`** yoki **`md`** buyrug‘idan foydalaning:
```cmd
mkdir yangi_katalog
```
Katalogga Kirish va Undan Chiqish
 - Katalogga kirish uchun **`cd`** buyrug‘idan foydalaning:
```cmd
cd yangi_katalog
```
 - Katalogdan chiqish uchun **`cd ..`** yoziladi:
```cmd
cd ..
```
Katalogni O‘chirish
Bo‘sh kataloglarni o‘chirish uchun **`rmdir`** buyrug‘i ishlatiladi:
```cmd
rmdir yangi_katalog
```
Agar katalog bo‘sh bo‘lmasa va uni o‘chirish kerak bo‘lsa, quyidagi buyruqdan foydalaning:
```cmd
rmdir /s /q yangi_katalog
```
### 4. Qo‘shimcha Kengaytirilgan Buyruqlar
 - **`tree`** – Katalog ichidagi fayl va papkalarni daraxt shaklida ko‘rsatadi:
```cmd
tree C:\foydalanuvchi\hujjatlar
```
 - **`ren`** – Fayl yoki katalog nomini o‘zgartiradi:
```cmd
ren eski_fayl.txt yangi_fayl.txt
```
### 5. Maslahat va Eng Yaxshi Amaliyotlar
 - Fayllarni o‘chirishda ehtiyot bo‘ling – Fayl o‘chirib bo‘lingandan so‘ng, uni qaytarish imkonsiz.
 - **`/s`** bayrog‘idan foydalanishdan avval ehtiyot bo‘ling – U barcha ichki fayl va kataloglarni o‘chiradi.
 - Buyruqlarni Administrator sifatida ishga tushiring, agar tizim kataloglari va fayllar bilan ishlash kerak bo‘lsa.
Ushbu qo‘llanma yordamida CMD yordamida fayllar va kataloglarni boshqarish bo‘yicha keng qamrovli bilimga ega bo‘lasiz. Har bir buyruq bilan tanishib, ularni amalda qo‘llash orqali CMD ni chuqurroq o‘rganishingiz mumkin.

