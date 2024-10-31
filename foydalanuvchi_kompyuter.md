# CMD orqali Foydalanuvchi va Kompyuter Ma'lumotlari

Ushbu qo'llanma CMD orqali foydalanuvchi va kompyuter haqida asosiy ma'lumotlarni olish va tahlil qilish uchun ishlatiladigan buyruqlar haqida tushuncha beradi.

## Mavzular

1. [Foydalanuvchi Haqida Ma'lumot](#foydalanuvchi-haqida-ma-lumot)
2. [Kompyuter Haqida Ma'lumot](#kompyuter-haqida-ma-lumot)
3. [Joriy Foydalanuvchi Sessiyasi](#joriy-foydalanuvchi-sessiyasi)
4. [Kompyuter Nomini Aniqlash](#kompyuter-nomini-aniqlash)
5. [Qo'shimcha Buyruqlar](#qo-shimcha-buyruqlar)

---

### 1. Foydalanuvchi Haqida Ma'lumot

Foydalanuvchi hisoblari va ular bilan bog'liq ba'zi ma'lumotlarni olish uchun quyidagi buyruqlar ishlatiladi.

#### `whoami` buyrug'i

**whoami** buyrug'i joriy foydalanuvchi nomini ko'rsatadi.

```bash
whoami
```
📘 Izoh: Bu buyruq joriy tizimda ishlatilayotgan foydalanuvchi hisobini qaytaradi.

**``net user``** buyrug'i

net user buyrug'i tizimdagi barcha foydalanuvchi hisoblarini ro'yxatlaydi yoki foydalanuvchi haqida batafsil ma'lumot beradi.

```cmd
net user
```
Misol: Muayyan foydalanuvchi haqida ma'lumot olish uchun quyidagi tarzda ishlatiladi:

```cmd
net user [foydalanuvchi_ismi]
```
📘 Izoh: Bu buyruq foydalanuvchining yaratilgan sanasi, oxirgi kirish va boshqa xususiyatlarni ko'rsatadi.

2. Kompyuter Haqida Ma'lumot
**`systeminfo`** buyrug'i

systeminfo buyrug'i kompyuterning texnik parametrlari haqida keng ma'lumot beradi.

```cmd
systeminfo
```
📘 Izoh: Bu buyruq OS versiyasi, RAM hajmi, protsessor turi va boshqa tizim ma'lumotlarini beradi.

**`hostname`** buyrug'i
hostname buyrug'i kompyuterning nomini qaytaradi.

```cmd
hostname
```
📘 Izoh: Bu buyruq ayniqsa tarmoqdagi kompyuterlarni ajratish uchun foydali.

3. Joriy Foydalanuvchi Sessiyasi
**`query user`** buyrug'i

query user buyrug'i joriy tizimda ochiq bo'lgan foydalanuvchi sessiyalari haqida ma'lumot beradi.

```cmd
query user
```
📘 Izoh: Bu buyruq yordamida foydalanuvchining sessiya nomi, holati va oxirgi faollik vaqti ko'rsatiladi.

4. Kompyuter Nomini Aniqlash
**`wmic computersystem get name`** buyrug'i

wmic yordamida kompyuter nomini olish mumkin.

```cmd
wmic computersystem get name
```
📘 Izoh: Bu buyruq tizim nomini qaytaradi va u boshqa kompyuterlar bilan tarmoq orqali muloqotda muhimdir.

5. Qo'shimcha Buyruqlar
**`tasklist buyrug'i`**

tasklist buyrug'i joriy tizimda ishlayotgan barcha jarayonlarni ro'yxatlaydi.

```cmd
tasklist
```
📘 Izoh: Bu buyruq yordamida jarayon nomlari va ularning PID (Jarayon Identifikatori) ko'rinadi.

**`getmac`** buyrug'i

getmac buyrug'i kompyuterning MAC manzilini ko'rsatadi.

```cmd
getmac
```
📘 Izoh: Bu buyruq kompyuterdagi tarmoq interfeyslarining MAC manzillarini ko'rsatadi.

---
Ushbu qo'llanma CMD orqali foydalanuvchi va kompyuter haqidagi ma'lumotlarni olishda keng qo'llaniladigan buyruqlarni o'z ichiga oladi. Har bir buyruq tizim bilan bog'liq asosiy ma'lumotlarni olish uchun juda foydali.
