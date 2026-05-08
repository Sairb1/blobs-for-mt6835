# 📦 Blobs for Realme 11 / 11x / Narzo 60x / C67 5G (MT6835)

This repository contains extracted **ramdisk blobs** intended for:

* TWRP builds
* Android 15 development
* OTA Version: RMX378X.15.0.0.1800
* AOSP / custom ROM development
* Vendor_boot ramdisk extraction

⚠️ Use at your own risk. These are raw extracted blobs and may require adaptation depending on your tree and Android base.

---

## 📱 Device Compatibility

* Realme 11
* Realme 11x
* Narzo 60x
* C67 5G
* Chipset: MT6835

---

## 📦 Required Firmware

Required firmware base:

`RMX378X_15.0.0.1800(EX01)`

Using mismatched firmware may break compatibility.

---

## 📂 Repository Structure

```text
ramdisk.cpio
```

or

```text
ramdisk.cpio.gz
```

---

## ⚙️ How to Extract Ramdisk

### Decompress

```bash
gzip -d ramdisk.cpio.gz
```

### Extract

```bash
mkdir ramdisk
cd ramdisk
cpio -idmv < ../ramdisk.cpio
```

---

## 🔁 Repack Ramdisk

```bash
find . | cpio -o -H newc > ../ramdisk.cpio
gzip ../ramdisk.cpio
```

---

## 🧠 Notes

* Extracted from stock vendor_boot
* Suitable for recovery/TWRP bringup
* Useful for init debugging and Android 15 migration
* Do not upload fully extracted ramdisk folders to GitHub

---

## 📢 Community

Telegram:
https://t.me/realme11x

---

## ⚠️ Disclaimer

Provided for educational and development purposes only.

You are responsible for any damage caused by modifying or flashing these files.
