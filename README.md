<div align="center">

# OnePlus 12R — TWRP + KernelSU (ksun) + SUSFS

Ограниченный TWRP и кастомное ядро с драйвером **ksun** и патчем **susfs** для **OnePlus 12R** на **OxygenOS 15**



![Device](https://img.shields.io/badge/Device-OnePlus%2012R-red)




![OS](https://img.shields.io/badge/OxygenOS-15-blue)




![Kernel](https://img.shields.io/badge/Kernel-5.15.149-green)




![ksun](https://img.shields.io/badge/ksun-2.3.0-orange)




![susfs](https://img.shields.io/badge/susfs-2.2.0-purple)



<img src="images/banner.png" alt="Banner" width="600">

</div>

---

## 📖 О проекте

Здесь собраны:

- **TWRP** — ограниченная сборка для OnePlus 12R
- **Ядро** с драйвером **ksun** (KernelSU-Next) и патчем **susfs**

Всё это нужно для получения root-доступа со скрытием следов root на OxygenOS 15.

<img src="images/overview.png" alt="Overview" width="300">

---

## 📦 Версии

| Компонент | Версия |
|-----------|--------|
| Устройство | OnePlus 12R |
| Прошивка | OxygenOS 15 |
| Ядро | **5.15.149** |
| ksun | **2.3.0** |
| susfs | **2.2.0** |

> ⚠️ Версия ядра на устройстве должна быть строго **5.15.149**. Проверить: `uname -r`

<img src="images/kernel_version.png" alt="Kernel version" width="300">

---

## ⚠️ Ограничения TWRP

Это **ограниченная** сборка TWRP:

- ❌ Раздел `/data` **не монтируется**
- ❌ `/sdcard` **не монтируется**
- Из-за этого часть функций не работает (бэкап/восстановление данных, файловый менеджер, установка zip с накопителя и т.д.)

<img src="images/twrp_limits.png" alt="TWRP limitations" width="300">

### ✅ Решение

Сбросить и пропатчить `/data` для расшифровки:

1. Сделай **полный factory reset** (⚠️ **все данные будут удалены!**)
2. Примени патч `/data` для расшифровки
3. После этого `/data` и `/sdcard` смогут монтироваться

<img src="images/factory_reset.png" alt="Factory reset" width="300">

---

## 🚀 Установка

> ⚠️ Перед началом обязательно сделай резервную копию важных данных.

### Требования

- Разблокированный загрузчик
- OnePlus 12R с OxygenOS 15
- Ядро версии 5.15.149
- ADB и Fastboot на ПК

### Шаги

1. Загрузи устройство в fastboot
2. Загрузи или прошей TWRP
3. Прошей ядро с ksun + susfs
4. Установи менеджер KernelSU-Next
5. Проверь работу root и susfs

<img src="images/install.png" alt="Installation" width="300">

---

## ✅ Проверка

- В менеджере отображается **ksun 2.3.0**
- susfs активен, версия **2.2.0**
- `uname -r` показывает **5.15.149**

<img src="images/manager.png" alt="KernelSU manager" width="300">

---

## ❗ Отказ от ответственности

Вы делаете всё **на свой страх и риск**. Автор не несёт ответственности за:

- потерю данных
- «кирпич» устройства
- потерю гарантии

---

## 🙏 Благодарности

- [KernelSU-Next](https://github.com/KernelSU-Next/KernelSU-Next)
- [susfs4ksu](https://gitlab.com/simonpunk/susfs4ksu)
- [TWRP](https://twrp.me/)

---

<div align="center">

⭐ Если проект помог — поставь звезду!

</div>
