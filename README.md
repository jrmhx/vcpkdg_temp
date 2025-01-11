# A template profile config for using vcpkg for C++ projects

[vcpkg](https://github.com/microsoft/vcpkg) is a package manager for C++ maintained by Microsoft.

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

## Setup in CLion

1. Open the project in CLion
2. Go to File → Settings → Build, Execution, Deployment → CMake (or CLion Preferences on macOS). 
3. In the CMake Profiles section:
   1. Select your active profile (e.g., Debug or Release). 
   2. In the CMake Options field, add:
      `-DCMAKE_TOOLCHAIN_FILE=${VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake`
