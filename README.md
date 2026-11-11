# Sharpa Wave

 Sharpa Wave is the official application for device configuration, monitoring, firmware updates, and routine operations.

---

## 📥 Download

Download the latest `.deb` package from Releases:

👉 https://github.com/sharpa-robotics/sharpa-wave/releases

---

## 🚀 Installation (Ubuntu)

Install the package using:

```bash
sudo dpkg -i sharpa-wave-<version>.deb
```

If there are missing dependencies, run:

```bash
sudo apt-get install -f
```

---

## ▶️ Run

After installation, you can launch the application:

```bash
sharpa-wave
```

Or find it in your application menu.

---

## 📦 SDK (Linux)

Sharpa Wave ships with a **matched Sharpa Wave SDK** and manages it automatically.

### Do not override the SDK used by Wave

- **Do not** install, upgrade, or replace `sharpa-wave-sdk` on your own.
- **Do not** copy or edit files under `/opt/sharpa-wave-sdk/` or `/opt/sharpa-wave/wave_sdk` (binaries, `config.yaml`, libraries, etc.) expecting Wave to keep using your changes.

To change the SDK version that Wave uses, **only upgrade or reinstall `sharpa-wave`** (same `.deb` workflow as in [Update](#-update)). That is the supported path.

### Where files live (reference)

After `sharpa-wave` installed, typical layout:

| Item | Path |
|------|------|
| Wave application | `/opt/sharpa-wave/` |
| Wave SDK root (what Wave prefers) | `/opt/sharpa-wave-sdk/` |
| `wave` service binary | `/opt/sharpa-wave-sdk/wave_sdk`, with a copy at `/opt/sharpa-wave/wave_sdk` |

Under `/opt/sharpa-wave-sdk/` you may see `wave_sdk`, `config.yaml`, `VERSION`, `lib/`, `python/`, `include/`, `sample/`. Treat these as **managed by the Wave installer**, not as a user-editable SDK install.

### Uninstall

Removing `sharpa-wave` also removes `/opt/sharpa-wave-sdk` and the `sharpa-wave-sdk` package. That is expected; reinstall `sharpa-wave` if you need Wave and its SDK again.

---

## 🔄 Update

To upgrade to a newer version:

```bash
sudo dpkg -i sharpa-wave-<new-version>.deb
```

---

## ❌ Uninstall

To remove the application:

```bash
sudo dpkg -r sharpa-wave
```

---

## ⚠️ Requirements

- Ubuntu 20.04 / 22.04
- x86_64 architecture

---

## 📌 Notes

- This is an internal tool for Sharpa Robotics
- Make sure the device is properly connected before running

---

## 📞 Support

For issues or questions, please contact the Sharpa Robotics development team.
