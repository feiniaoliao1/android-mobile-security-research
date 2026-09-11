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

## Conclusion
1. KernelSU LKM works at kernel level, different from Zygisk user-mode root.
2. Many root checks scan `/proc` and kernel log.
3. Hiding root needs to modify kernel layer trace, not only user space.
4. SukiSU-Ultra is also tested as an alternative kernel root solution.

## Statement
Only personal security learning. Not used for unauthorized or illegal purposes.

