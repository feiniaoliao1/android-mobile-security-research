# KernelSU Experiment on OnePlus 13T

## Experiment Overview
Study KernelSU LKM root, SukiSU-Ultra, root detection, SELinux mode, and root hiding theory.

## Environment
- Device: OnePlus 13T
- Root solution: KernelSU (LKM&GKI), SukiSU-Ultra（GKI）
- Test tools: su, top, dmesg, LSPosed

## Key Operation
1. Patch init_boot.img and flash KernelSU into init_boot partition.
2. Use su command to get root shell, check process and system load.
3. Test SELinux permissive/enforcing switch.
4. Research root detection methods: detect su binary, check kernel symbols.
5. Try to hide root traces for app environment detection research.

## Risk & Impact Analysis
Unlocking bootloader and root will break device trusted environment. Banking and game applications may detect modification and restrict service. Root hiding only bypass partial user-space checks, hardware-backed attestation cannot be bypassed by pure software method.

## Detection & Defense Mechanisms
1. Common user-space root detection: check su binary, check magisk related props, scan process list. These methods can be bypassed by KernelSU hide feature.
2. Deeper detection: kernel space behavior monitoring, verified boot, TEE attestation. Those are harder to bypass.
3. Defense suggestion: app can combine multi-layer detection (userland + kernel attestation) to identify modified device.


## Conclusion
1. KernelSU LKM works at kernel level, different from Zygisk user-mode root.
2. Many root checks scan `/proc` and kernel log.
3. Hiding root needs to modify kernel layer trace, not only user space.
4. SukiSU-Ultra is also tested as an alternative kernel root solution.

## Statement
Only personal security learning. Not used for unauthorized or illegal purposes.

