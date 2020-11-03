# ASUS-B360M-i5 8600k-OC0.6.4

- 不是自己编译版 基本包为 独行秀才 和 williambj1 的编译包 感谢二位大神

- 支持核显自动识别 经测试 boot-args：igfxfw=2 npci=0x3000 就可以自动驱动核显

- 下载系统和系统写入u盘可以看看上面的[wiki](https://gitee.com/k2y1982/opencore/wikis)。

# **为配合big sur 11.0.1安装特性已做如下修改：** 

- 最新版的11.0.1支持中文安装了，但 SecureBootModel 还是要设置为 Disabled

- 如果你还是beta10的镜像请将 NVRAM - 7C436110-AB2A-4BBB-A880-FE41995C9F82 - prev-lang:kbd 已设置为英语 656E2D55533A30

- 如果你之前已经安装过macOS，在更改efi后，请在oc的辅助项里 使用一次 reset_NVRAM 以清理 NVRAM。

- 不然会遇到-v代码跑完-进度条跑完后只有灰屏和鼠标(big sur beta10 全新安装时)。

# **如果你是安装 Catalina 可以将：** 

- 1.Misc - Security - SecureBootModel 已设置为 Default

- 2.NVRAM - 7C436110-AB2A-4BBB-A880-FE41995C9F82 - prev-lang:kbd 已设置为中文(默认已改回中文) 7A682D48 616E733A 323532

- 这样就不会遇到挂在efi分区时occ卡死的问题。

# **目前版本为：** 

 **2020-11-3 OC 0.6.4 by 独行秀才**

- 更新内容：
- 更新版本号为0.6.4

 **2020-11-3 OC 0.6.4 by williambj1**

- 更新内容：
- Bump version to 0.6.4

 **2020-11-1 OC 0.6.3 by 独行秀才**

- 更新内容：
- 给一些X299主板上的只读错误增加了解决方案
- 增加了对x86legacy安全引导模型的支持

 **2020-10-30 OC 0.6.3 by 独行秀才**

- 更新内容：
- 修正了Ps2MouseDxe在OpenDuetPkg下未正确加载

 **2020-10-30 OC 0.6.3 by williambj1**

- 更新内容：
- DataBase: Updated builtin firmware versions
- OcConsoleLib: Improve error reporting with TextoutputBuiltin (#143)

 **2020-10-29 OC 0.6.3 by williambj1**

- 更新内容：
- DataBase: Updated builtin firmware versions
- DataBase: Update MM71

 **2020-10-28 OC 0.6.3 by williambj1**

- 更新内容：
- Patches: Fix previous commit
- Patches: Add PS/2 mouse patch for SioBusDxe

 **2020-10-28 OC 0.6.3 by 独行秀才**

- 更新内容：
- 添加ForceResolution选项以启用非默认分辨率

 **2020-10-27 OC 0.6.3 by williambj1**

- 更新内容：
- Docs: Fixed typo
- Docs: Rebuild pdf and update changelog
- VBIOS patching via ForceResolution option (#144)

 **2020-10-26 OC 0.6.3 by 独行秀才**

- 更新内容：
- 修正了在选择MacPro5,1时的扫描策略 NVMe的问题
- 修复了平台上的I/O无法读取超过1MB的问题
- 修复了在Big Sur上plist-only kext注入的问题

 **2020-10-26 OC 0.6.3 by williambj1**

- 更新内容：
- Docs: Update changelog

 **2020-10-25 OC 0.6.3 by williambj1**

- 更新内容：
- OcAppleKernelLib: Rebuild KC when no kexts are injected
- OcAppleKernelLib: Fix invalid kremlin section
- OcFileLib: Actually fix MSVC warnings
- OcAppleKernelLib: Zero trailing KC expansion
- OcFileLib: Silence MSVC
- OcFileLib: Fixed I/O issues on platforms incapable of reading over 1MB
- Docs: Add errata entry for 11.0 b10
- Patches: Fix warning with newer git client version
- OcBootManagementLib: Fixed ScanPolicy NVMe handling on MacPro5,1

 **2020-10-24 OC 0.6.3 by 独行秀才**

- 更新内容：
- 例行更新

 **2020-10-22 OC 0.6.3 by 独行秀才**

- 更新内容：
- 修正了老旧Atom cpu检测的问题

 **2020-10-21 OC 0.6.3 by williambj1**

- 更新内容：
- OcCpuLib: Add compatibility for Bonnell Atom CPUs
- OcCpuLib: First-gen Atom does not support TURBO_RATIO_LIMIT MSR
