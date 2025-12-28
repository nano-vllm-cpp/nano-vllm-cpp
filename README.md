# nano-vllm-cpp
Nano vLLM

## Build (CMake + vcpkg)

This project is configured for C++20 and can optionally use a local `vcpkg` checkout.

Quick steps:

1. Bootstrap vcpkg (if you want to use it):

```bash
git clone https://github.com/microsoft/vcpkg.git vcpkg
cd vcpkg
./bootstrap-vcpkg.sh
cd ..
```

2. Install packages with vcpkg (example `fmt`):

```bash
./vcpkg/vcpkg install fmt
```

3. Configure and build with CMake (out-of-source):

```bash
mkdir -p build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
cmake --build . --config Release
```

If you placed `vcpkg` in the repository root the CMakeLists will automatically use
`vcpkg/scripts/buildsystems/vcpkg.cmake` as a toolchain file.

Run the produced executable:

```bash
./nano_app
```
