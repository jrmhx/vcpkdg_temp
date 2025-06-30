# A template profile config for using vcpkg for C++ projects

## Install and Setup vcpkg
[install vcpkg and set up cmake profiles](https://learn.microsoft.com/en-us/vcpkg/get_started/get-started-vscode?pivots=shell-bash)

```bash
git clone https://github.com/microsoft/vcpkg.git
cd vcpkg
./bootstrap-vcpkg.sh
```

add the export command to your shell's profile script (e.g., ~/.bashrc or ~/.zshrc).

```bash
export VCPKG_ROOT=/the/actual/path/to/vcpkg
export PATH=$PATH:$VCPKG_ROOT
```

```text
   -DCMAKE_TOOLCHAIN_FILE=${VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake
```
