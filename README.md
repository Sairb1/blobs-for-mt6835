# 📦 Blobs for Realme 11 / 11x / Narzo 60x / C67 5G (MT6835)

This repository contains extracted **ramdisk blobs** intended for:

* TWRP builds
* AOSP / custom ROM development

⚠️ **Use at your own risk.** These files are raw dumps and may require adaptation depending on your tree and Android base.

---

## 📱 Device Compatibility

* Realme 11
* Realme 11x
* Narzo 60x
* C67 5G
* Chipset: MT6835

---

## 📦 Required Firmware

You must be on the exact base:

**OTA Version:** `RMX378X_14.0.0.115(EX01)`

Using mismatched firmware will break compatibility.

---

## 📂 Repository Structure

```
ramdisk.cpio.gz
```

---

## ⚙️ How to Extract Ramdisk

### 1. Decompress

```
gzip -d ramdisk.cpio.gz
```

### 2. Extract CPIO

```
mkdir ramdisk
cd ramdisk
cpio -idmv < ../ramdisk.cpio
```

---

## 🔁 How to Repack Ramdisk

After making changes:

```
find . | cpio -o -H newc > ../ramdisk.cpio
gzip ../ramdisk.cpio
```

---

## 🧠 Notes

* Built from stock vendor_boot
* Suitable for recovery and early init debugging
* Do NOT push raw extracted ramdisk to GitHub (breaks structure & compatibility)

---

## 📢 Community

Telegram Group: https://t.me/realme11x

---

## ⚠️ Disclaimer

This is provided for development and educational purposes only.
Flashing or modifying these files may brick your device.

You are responsible for what you do with them.
