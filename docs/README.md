## *KernelSU*

<img src="https://kernelsu.org/logo.png" style="width: 96px;" alt="logo">A kernel-based root solution for Android devices.

---

## 🔧 KernelSU Integration (Recommended)

This project uses an enhanced integration method based on
"Backslashxx/KernelSU" (https://github.com/backslashxx/KernelSU).

## 🚀 Quick Setup

Run this inside your kernel source:

```sh
curl -LSs "https://raw.githubusercontent.com/Mr-Morat/KernelSU-Next/stable/kernel/setup.sh" | bash -s syscall
```

This will automatically integrate KernelSU using the syscall method.

---

✅ Supported Implementations

- tian/KernelSU-Official
- backslashxx/xxksu
- KOWX712/KowSU
- rifsxd/KernelSU-Next
- rsuntk/RKSU
- RapliVx/MamboSU
- WildKernels/WildKSU

---

## ⚙️ Requirements

Before building your kernel:

- Remove all manual hook implementations (to avoid conflicts)

- Disable:
```config
CONFIG_KPROBES=n
```

- Enable:
```config
CONFIG_KSU=y
CONFIG_KSU_TAMPER_SYSCALL_TABLE=y
```

- Optional (for extra features like AVC log spoofing):
```config
CONFIG_KSU_EXTRAS=y
```


---

## 📝 Integration Notes

- Recommended to use a clean kernel source
- Do not mix with other hooking methods
- Always perform a full rebuild after changing configs