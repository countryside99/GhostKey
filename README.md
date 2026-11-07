# GhostKey
One-tap ephemeral root through CVE-2026-98260 vulnerability (GhostKey) on selected devices.

> [!IMPORTANT]
> Root is **ephemeral**. The kernel module, `su` and any loaded modules are gone the moment the
> device reboots. A reboot always returns the phone to a clean, unrooted state - which is also the
> recovery path if a run goes wrong.

## How to use
- Install the GhostKey APK from [Releases](https://github.com/mitschud/DirtyFrag/releases/latest)
- Grant Shizuku Permission
- Install a SU Manager that **ships** libksud.so:
  - Samsung - **required**:
     - [diabl0w's KernelSU](https://github.com/diabl0w/KernelSU/releases)
   - Other:
     - [KernelSU](https://github.com/tiann/KernelSU/releases/latest)
     - [KernelSU-Next](https://github.com/KernelSU-Next/KernelSU-Next/releases/latest)
     - [KowSU](https://github.com/KOWX712/KernelSU/releases/latest)
     - [BakaSU](https://github.com/Baka-SU/BakaSU/releases/latest) (formerly ReSukiSU)
     
  3. Open GhostKey, choose your SU Manager, then press **Run exploit**.
## Supported Devices
| Device | Model | Kernel version & Firmware | Status |
| --- | --- | --- | --- |
| `Samsung Galaxy S25 Ultra` | SM-S938B | `6.6.127` One UI 9, Android 17 | 2026-10-05 Security Patches Ongoing porting |

More devices **coming**, I currently don't have a lot of devices for testing, but I can guarantee support in my free time for S25 Ultra 'till the exploit gets patched, since it's my device!
If you wanna help me, you can open a Pull Request and add a payload for your device!
Also, if you're just a user and you have **higher** security patches versions than the current reported status, then submit an issue so I can update the status!
## Credits
- **CVE-2026-98260-aurora** — this app is built on the `aurora` repo's timer
  LPE port: the `timer.c` payload (real-cred zero-write and fake-cred /
  ksud late-load chains) started there and lives in this project as
  `app/src/main/cpp/timer.c`
- [**SamTimer**](https://github.com/yoro1836/SamTimer) - Upstream source
-   [DirtyFrag](https://github.com/mitschud/DirtyFrag) (CVE-2026-43284, DFRoot
  lineage) — the autorun / failed-run-interlock pattern
- [Shizuku](https://github.com/RikkaApps/Shizuku) — shell-uid execution
  without a PC
## LICENSE
The project is licensed under GPL 2.0 license
## Responsibility Disclosure


## Your warranty is now void.

 **I am not responsible for bricked devices, dead SD cards,
 thermonuclear war, or you getting fired because the alarm app failed. Please
 do some research if you have any concerns about features included in this software
 before flashing it! YOU are choosing to make these modifications, and if
 you point the finger at me for messing up your device, I will laugh at you.**
