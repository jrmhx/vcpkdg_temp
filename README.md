# A template profile config for using vcpkg for C++ projects

## What is this?

[vcpkg](https://github.com/microsoft/vcpkg) is a package manager for C++ libraries, it's maintained by Microsoft.

Combining it with CMake, you can manage dependencies for your C++ projects like using `cargo` for Rust. However, it's still not as good as `cargo` tho, but basically not bad as we have for C++ now in my opinion.

One of the most downside of `vcpkg` compared to `cargo` is the tricky init setup process to build run and debug your project in IDEs. So I create this repo to reserve the setup process for my future projects' use.

## Prerequisites

- [install vcpkg and set up cmake profiles](https://learn.microsoft.com/en-us/vcpkg/get_started/get-started-vscode?pivots=shell-bash)
- [install CLion](https://www.jetbrains.com/clion/download/)

## Setup in JetBrains CLion

- Open the project in CLion
- Go to `File` -> `Settings` -> `Build, Execution, Deployment` -> `CMake`
- Enable `default` profile
- In `Debug` profile, add `-DCMAKE_TOOLCHAIN_FILE=<path-to-vcpkg>/scripts/buildsystems/vcpkg.cmake` to `CMake options`
- Apply the changes
