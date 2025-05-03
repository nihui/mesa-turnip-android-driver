# mesa turnip android driver
mesa turnip driver for android

Download prebuilt binary at https://github.com/nihui/mesa-turnip-android-driver/releases/latest

This turnip driver library can be used with ncnn vulkan loader [simplevk.h](https://github.com/Tencent/ncnn/blob/master/src/simplevk.h)

```cpp
#include "simplevk.h"

ncnn::load_vulkan_driver("libvulkan_freedreno.so");

// now you call any global vulkan functions
// ncnn::vkGetInstanceProcAddr
// ncnn::vkEnumerateInstanceExtensionProperties
// ncnn::vkCreateInstance
// ncnn::vkEnumerateInstanceLayerProperties

// any vulkan api entrypoint can be retrieved from vkGetInstanceProcAddr

ncnn::unload_vulkan_driver();
```

- Hot-swap android vulkan driver at runtime
- Full support for Adreno 6xx/7xx series
- Better performance than the system blobs
- Can be used directly in your application
- All vulkan extensions implemented are enabled
- Support Android 8.0 or later

# Credits
- https://gitlab.freedesktop.org/mesa/mesa for mesa turnip driver source
- https://github.com/v3kt0r-87/Mesa-Turnip-Builder for mesa turnip build instruction
- https://github.com/lizhangqu/dlfcn_compat for dlopen android system library
