🙌👍Getting into java.
😁If you want to jailbreak something, email me because I want to help/learn samjoe2010.s@gmail.com
SC490 Jethro Firmware!  This does not inlcude the userdata.img.  I do not reccomend full flash.
# 📱 SC490 Dumbphone Firmware Dump & Notes
Firmware is here > https://drive.google.com/file/d/15glP9zp6oW5zboZGmp7MAclDeX0Bp9Oh/view?usp=sharing

This repository contains a firmware dump and technical notes for the SC490 flip phone. This device runs a MediaTek chipset and is commonly sold under the Jethro brand. The dump was created using **`mtkclient`**, not SP Flash Tool.

---

## 🚨 Important Notes

- ⚠️ **Do NOT attempt a full flash** unless you know what you're doing. The firmware is incomplete and doing a full flash may **soft-brick** your device (plus why you do that lol I havent modified anything).
- ⚠️ **`userdata.img` is missing** from this repository but will be added soon.
- ✅ Use **`mtkclient`** for all operations — **not SP Flash Tool**.
- ⚠️ This firmware is for exploration, development, and recovery purposes only. Use at your own risk.

---

## 📦 Notable Files Included

| Filename      | Description                                     |
|---------------|-------------------------------------------------|
| `preloader.bin` | MediaTek preloader required for boot          |
| `boot.img`    | Boot partition containing kernel & ramdisk       |
| `lk.img`      | Little Kernel (bootloader)                      |
| `system.img`  | System partition with OS & applications         |
| `MT6739_Android_scatter.txt`  | Partition layout for dumping and flashing         |




---

## ⚙️ Boot Behavior and Partition Notes

- `boot.img` contains a `default.prop` that **points to another file closely named the same prop.default inside `system.img\etc\`**. That second file controls the actual runtime properties like `ro.debuggable`, `ro.adb.secure`, etc.


---

## 🔧 Flashing

Use [mtkclient](https://github.com/bkerler/mtkclient) to interact with the device.
SP Flash Tool works with flashing but I had problems dumping the data with this tool, let me know if its just me or if SP Tool doesnt work right by Emailing me at samjo2010.s@gmail.com
README.md made with chatgpt (I LOVE CHATGPT) and edited by Garbagebuild

