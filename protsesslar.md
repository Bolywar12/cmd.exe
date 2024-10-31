# CMD orqali Protsesslarni Boshqarish

Ushbu qo'llanma CMD yordamida Windows tizimida protsesslarni boshqarish, monitoring qilish va tahlil qilish uchun asosiy buyruqlarni o'z ichiga oladi.

## Mavzular

1. [Protsesslar Ro'yxati](#protsesslar-ro-yxati)
2. [Muayyan Protsessni Topish](#muayyan-protsessni-topish)
3. [Protsessni To'xtatish](#protsessni-to-xtatish)
4. [Protsess Prioritetini O'zgartirish](#protsess-prioritetini-o-zgartirish)
5. [Qo'shimcha Buyruqlar](#qo-shimcha-buyruqlar)

---

### 1. Protsesslar Ro'yxati

#### `tasklist` buyrug'i

**tasklist** buyrug'i joriy tizimda ishlayotgan barcha protsesslarni ro'yxatlash uchun ishlatiladi.

```bash
tasklist
```
📘 Izoh: Bu buyruq yordamida protsess nomi, PID (Jarayon Identifikatori), va xotira miqdori kabi ma'lumotlarni olish mumkin.

2. Muayyan Protsessni Topish
tasklist /fi buyrug'i
tasklist /fi buyrug'i yordamida filtr orqali muayyan protsesslarni topish mumkin.

bash
Копировать код
tasklist /fi "imagename eq [protsess_nomi]"
Misol:

bash
Копировать код
tasklist /fi "imagename eq chrome.exe"
📘 Izoh: Bu buyruq yordamida tizimdagi muayyan dastur yoki jarayon nomiga mos protsessni topish mumkin.

3. Protsessni To'xtatish
taskkill buyrug'i
taskkill buyrug'i muayyan protsessni PID yoki nom orqali to'xtatish uchun ishlatiladi.

bash
Копировать код
taskkill /pid [PID]
yoki

bash
Копировать код
taskkill /im [protsess_nomi]
Misollar:

PID orqali protsessni to'xtatish:

bash
Копировать код
taskkill /pid 1234
Protsess nomi orqali to'xtatish:

bash
Копировать код
taskkill /im notepad.exe
📘 Izoh: taskkill /f parametri protsessni majburiy to'xtatadi.

4. Protsess Prioritetini O'zgartirish
wmic process buyrug'i
wmic process yordamida protsesslarning prioritetini o'zgartirish mumkin.

bash
Копировать код
wmic process where name="[protsess_nomi]" CALL setpriority "[prioritet]"
Misollar:

A'lo daraja (Realtime): 256
Yuqori daraja (High): 128
Normal daraja (Normal): 32
Past daraja (Low): 16
Misol:

bash
Копировать код
wmic process where name="notepad.exe" CALL setpriority "128"
📘 Izoh: Bu buyruq yordamida dasturlar prioritet darajasini sozlash orqali ularning tizim resurslariga ta'sirini boshqarish mumkin.

5. Qo'shimcha Buyruqlar
get-process buyrug'i (PowerShell)
CMD bilan bir qatorda, PowerShell orqali ham protsesslarni boshqarish mumkin.

Protsesslar ro'yxati:

powershell
Копировать код
get-process
Muayyan protsessni to'xtatish:

powershell
Копировать код
stop-process -name [protsess_nomi]
start buyrug'i
start buyrug'i yordamida yangi dastur yoki protsessni ishga tushirish mumkin.

bash
Копировать код
start [dastur_nomi]
Misol:

```cmd
start notepad.exe
```
📘 Izoh: Ushbu buyruq yordamida muayyan dasturlarni CMD orqali bevosita ishga tushirish mumkin.

---
Ushbu qo'llanma CMD yordamida protsesslarni kuzatish, boshqarish va o'zgartirish uchun eng keng tarqalgan buyruqlarni o'z ichiga oladi.
