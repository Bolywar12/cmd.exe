# CMD orqali Skriptlar Yaratish va Avtomatlashtirish

Ushbu qo'llanma Windows CMD orqali skript yaratish va vazifalarni avtomatlashtirish uchun foydalaniladigan asosiy buyruqlar va texnikalar haqida tushuncha beradi. Bu CMD yordamida takroriy vazifalarni avtomatlashtirishni osonlashtiradi.

## Mavzular

1. [Skriptlar Yaratish Kirish](#skriptlar-yaratish-kirish)
2. [Oddiy CMD Skript Yaratish](#oddiy-cmd-skript-yaratish)
3. [If/Else Shartli Operatorlar](#ifelse-shartli-operatorlar)
4. [For Tsiklidan Foydalanish](#for-tsiklidan-foydalanish)
5. [Rejalashtirilgan Vazifalar](#rejalashtirilgan-vazifalar)

---

### 1. Skriptlar Yaratish Kirish

CMD orqali .bat yoki .cmd kengaytmali fayllarni yaratish orqali skriptlar yozish mumkin. Bu fayllar buyruqlarni birgalikda ishlatishga imkon beradi va ular Windows orqali avtomatlashtirish uchun ishlatiladi.

**Misol:** Quyidagi kabi fayl yarating va `.bat` yoki `.cmd` kengaytmasi bilan saqlang.

---

### 2. Oddiy CMD Skript Yaratish

Quyidagi misolda oddiy bir skript ko'rsatiladi:

```bat
@echo off
echo "Bu CMD skripti"
pause
```
 - @echo off – Barcha buyruqlarni ekranga chiqarishni o'chiradi.
 - echo – Matnni ekranga chiqaradi.
 - pause – Skriptni davom ettirish uchun foydalanuvchidan tugma bosishni so'raydi.
📘 Izoh: Faylni .bat yoki .cmd kengaytmasi bilan saqlaganingizdan so'ng, uni ikki marta bosish orqali ishga tushirishingiz mumkin.

3. If/Else Shartli Operatorlar
if va else operatorlari shartli tekshiruvlar bajarishga yordam beradi.

Sintaksis:

```bat
if [shart] ( 
    echo "Shart bajarildi"
) else (
    echo "Shart bajarilmadi"
)
```
Misol: Foydalanuvchi kiritgan ma'lumotni tekshirish.

```bat
@echo off
set /p ism="Ismingizni kiriting: "
if %ism%==Ali (
    echo "Salom, Ali!"
) else (
    echo "Salom, %ism%!"
)
```

📘 Izoh: set /p foydalanuvchidan ma'lumot olish uchun ishlatiladi.

4. For Tsiklidan Foydalanish
for tsikli bilan bir nechta ma'lumotlarni ketma-ket ishlatish yoki fayllarni qayta ishlash mumkin.

Sintaksis:

```bat
for %%x in (1 2 3) do (
    echo "Qiymat: %%x"
)
```
Misol: Joriy katalogdagi barcha .txt fayllarni ko'rsatish.

```bat
@echo off
for %%f in (*.txt) do (
    echo Fayl nomi: %%f
)
```
📘 Izoh: for tsikli bilan fayl kengaytmalarini yoki boshqa qiymatlarni takrorlash mumkin.

5. Rejalashtirilgan Vazifalar
Windowsning Task Scheduler dasturi orqali avtomatlashtirilgan vazifalarni rejalashtirish mumkin. Buning uchun CMD dan schtasks buyrug'i foydalaniladi.

schtasks buyrug'i
schtasks yordamida skriptlarni yoki dasturlarni ma'lum vaqtga rejalashtirish mumkin.

Misol: Skriptni har kuni soat 12:00 da ishlatish uchun:

```bash
schtasks /create /tn "MeningVazifam" /tr "C:\yo'l\skriptim.bat" /sc daily /st 12:00
```
 - /tn – Vazifa nomi.
 - /tr – Ishlatiladigan skript yoki dastur yo'li.
 - /sc – Takrorlash turi (daily - har kuni).
 - /st – Ish vaqti (soat).

📘 Izoh: Ushbu buyruq Task Scheduler'da yangi rejalashtirilgan vazifa yaratadi va belgilangan vaqtga asosan ishlaydi.

---
Ushbu qo'llanma CMD orqali skript yaratish va avtomatlashtirishning asosiy texnikalarini o'z ichiga oladi. Yozilgan skriptlarni Windows Task Scheduler bilan birgalikda ishlatish orqali tizimning turli qismlarini avtomatlashtirish mumkin.
