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
