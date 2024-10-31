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