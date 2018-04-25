# How to compile libyuv

Libyuv is a subproject of chromium which is dedicated in image format conversion, for example from yuv420 to rgba.


> DON'T just clone the repository of libyuv, it won't work

Main idea:
Follow the instructions of `Getting Start` in the libyuv repository.

- Download the depot-tool
- Use the depot-tool to clone the sync libyuv codebase
- Use Cmake to generate VS Project after once the code is pulled down to local.
- Make sure the SIMD instruction is set to get hardware accelerations, e.g. SSE3
