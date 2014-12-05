LGE System
==========

https://github.com/neosmart/pevents project alternative which also includes threads and critical sections.
Main goal is performance, simplicity and minimal win32 code modification. Primary used for ray-trace Lion Game Engine.
Supported platforms: windows, linux, macos, android, ios.

There some limitations:
  1. WaitForMultipleObjects cannot be used with overlapped events set at the same time.
  2. WaitForMultipleObjects\WaitForSingleObject can wait only on events, mutexes and threads not supported.
  3. PulseEvent not supported bacause it's broken.
  4. WaitThread do not have timeout parameter because pthread_timedjoin_np not available on all platforms.

LGE System is developed and maintained by https://github.com/lieff
