# ASUS-B360M-i5 8600k-OC0.6.3
支持核显自动识别

为配合big sur beta10安装特性已做如下修改：

1.Misc - Security - SecureBootModel 已设置为 Disabled

2.NVRAM - 7C436110-AB2A-4BBB-A880-FE41995C9F82 - prev-lang:kbd 已设置为 656E2D55533A30(英语)

如果你之前已经安装过macOS，在更改efi后，请在oc的辅助项里 使用一次 reset_NVRAM 以清理 NVRAM。

不然会遇到-v代码跑完-进度条跑完后只有灰屏和鼠标(big sur beta10 全新安装时)。


如果你是安装 Catalina 可以将：

1.Misc - Security - SecureBootModel 已设置为 Default

2.NVRAM - 7C436110-AB2A-4BBB-A880-FE41995C9F82 - prev-lang:kbd 已设置为 7A682D48 616E733A 323532(中文)

这样就不会遇到挂在efi分区时occ卡死的问题。


目前版本为：

OC 0.6.3 2020-10-21 by williambj1

更新内容：

OcCpuLib: Add compatibility for Bonnell Atom CPUs

OcCpuLib: First-gen Atom does not support TURBO_RATIO_LIMIT MSR
