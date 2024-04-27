# Vulkan

## Installation
> [!NOTE]
> These installation steps are specifically designed for Unix machines. Functionality may vary on a Windows operating system.

Ensure that you have the [VulkanSDK](https://www.lunarg.com/vulkan-sdk/) installed to your device.

Using [git](https://git-scm.com/), clone this repository onto your device.

```bash
git clone https://github.com/Coincadink/Vulkan.git
```

Now, moving inside the project directory, propagate the git submodules into your project.

```bash
cd Vulkan
git submodule init
git submodule update
```

Finally, to build and run utilizing [CMake](https://cmake.org/):

```bash
mkdir build
cd build
cmake ..
make
./Vulkan
```