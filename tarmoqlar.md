# CMD da Tarmoqlar Bilan Ishlash

Ushbu qo'llanma CMD orqali tarmoq diagnostikasi, sozlamalari va boshqaruvi uchun foydalaniladigan asosiy buyruqlar va ularning qo'llanilish usullari haqida tushuncha beradi.

## Mavzular

1. [Ping Buyrug'i](#ping-buyrug-i)
2. [Ipconfig Buyrug'i](#ipconfig-buyrug-i)
3. [Tracert Buyrug'i](#tracert-buyrug-i)
4. [Netstat Buyrug'i](#netstat-buyrug-i)
5. [Nslookup Buyrug'i](#nslookup-buyrug-i)
6. [Netsh Buyrug'i](#netsh-buyrug-i)
7. [Pathping Buyrug'i](#pathping-buyrug-i)
8. [Qo'shimcha Ma'lumotlar](#qo-shimcha-ma-lumotlar)

---
### 1. Ping Buyrug'i

**Ping** buyruqlari tarmoqqa ulanadigan boshqa qurilmalarning mavjudligini tekshirishda qo'llaniladi.

**Sintaksis:**
```bash
ping [domen yoki IP]
```
Misol:
```cmd
ping google.com
```
ℹ Izoh: Bu buyruq ma'lum bir IP manzil yoki domenga bog'lanishning mavjudligini va kechikish vaqtini o'lchaydi.

### 2. Ipconfig Buyrug'i
Ipconfig buyrug'i tarmoq interfeyslari haqida ma'lumot olish va tarmoq sozlamalarini yangilash uchun ishlatiladi.

Sintaksis:

```cmd
ipconfig
```
Asosiy opsiyalar:
 - **`ipconfig`** /all – Qurilmadagi barcha tarmoq adapterlari haqida to'liq ma'lumot beradi.
 - **`ipconfig /release`** – Joriy IP manzilni bo'shatadi.
 - **`ipconfig /renew`** – IP manzilni yangilaydi.
 - **`ipconfig /flushdns`** – DNS keshini tozalaydi.
### 3. Tracert Buyrug'i
Tracert buyrug'i paketning manzilga boradigan yo'lini ko'rsatadi.

Sintaksis:

```cmd
tracert [domen yoki IP]
```
Misol:

```cmd
tracert google.com
```
ℹ Izoh: Bu buyruq paketning manzilga borishida o'tadigan marshrut haqida ma'lumot beradi.

### 4. Netstat Buyrug'i
Netstat buyruqlari ochiq portlar va faol ulanishlar haqida ma'lumot beradi.

Sintaksis:

```cmd
netstat [opsiyalar]
```
Asosiy opsiyalar:
 - **`netstat -a`** – Barcha ulanishlar va tinglayotgan portlarni ko'rsatadi.
 - **`netstat -n`** – IP va port raqamlarini raqamli formatda ko'rsatadi.
 - **`netstat -o`** – Har bir ulanish uchun jarayon ID (PID)ni ko'rsatadi.
### 5. Nslookup Buyrug'i
Nslookup buyrug'i DNS orqali IP yoki domen nomini tekshiradi.

Sintaksis:

```cmd
nslookup [domen yoki IP]
```
Misol:

```cmd
nslookup google.com
```
ℹ Izoh: Bu buyruq domen nomini IP manzilga yoki aksincha o'zgartirishga yordam beradi.

### 6. Netsh Buyrug'i
Netsh buyrug'i Windows tarmoq konfiguratsiyasini sozlash uchun ishlatiladi.

Sintaksis:

```cmd
netsh [buyruqlar]
```
Misollar:
 - **`netsh wlan show profile`** – Wi-Fi profil va parollarini ko'rsatadi.
 - **`netsh interface ip set address name="Local Area Connection" static [IP] [Subnet Mask] [Gateway]`** – IP manzilni statik qilib sozlaydi.
 - **`netsh advfirewall set allprofiles state off`** – Windows Firewall'ni o'chiradi.
### 7. Pathping Buyrug'i
Pathping buyrug'i **`ping`** va **`tracert`** funksiyalarini birlashtirib, har bir marshrut tugunining uzilish darajasini ko'rsatadi.

Sintaksis:

```cmd
pathping [domen yoki IP]
```
Misol:

```cmd
pathping google.com
```
ℹ Izoh: Bu buyruq har bir marshrut tuguni orqali o'tadigan paketlarning uzilish darajasini o'lchaydi.

### 8. Qo'shimcha Ma'lumotlar
 - CMD haqida: CMD bu Windows buyruqlar qatori bo'lib, foydalanuvchiga operatsion tizim bilan muloqot qilish imkonini beradi.
 - Qo'shimcha buyruqlar: CMD da boshqa ko'plab tarmoq buyruqlari mavjud bo'lib, ularga **`arp`**, **`ftp`**, **`telnet`** kabi buyruqlar kiradi.

---
Ushbu qo'llanma tarmoqlar bilan ishlash uchun CMD da eng keng qo'llaniladigan buyruqlarni o'z ichiga oladi.
