# Portage Configuration

This is my main portage configuration (for my desktop).

I use the following profile:

```
[24]  default/linux/amd64/17.1/desktop/plasma/systemd (stable) *
```

## Patches

I use a few different patches in order to my system

### x11-drivers/nvidia-drivers

- Disable check for PREEMPT\_RT scheduling in kernel
- Disable `wbindd` cache invalidation  
  This introduces a fair amount of latency whenever you start an OpenGL
  application. There doesn't seem to be any adverse effects by disabling it.

### app-emulation/wine-staging-4.21

- Allow emulation of system calls using seccomp (League of Legends 9.10+)

### sys-libs/glibc

- Add extra thread-local storage for the Wine syscall patch to use
