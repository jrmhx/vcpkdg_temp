# A template profile config for using vcpkg for C++ projects

## Prerequisites

- [install vcpkg and set up cmake profiles](https://learn.microsoft.com/en-us/vcpkg/get_started/get-started-vscode?pivots=shell-bash)

## Setup in JetBrains CLion

- Open the project in CLion
- Go to `File` -> `Settings` -> `Build, Execution, Deployment` -> `CMake`
- Enable `default` profile
- In `Debug` profile, add `-DCMAKE_TOOLCHAIN_FILE=<path-to-vcpkg>/scripts/buildsystems/vcpkg.cmake` to `CMake options`
- Apply the changes