# OpenXR SDK

1. OpenXR SDK must support:
- Conformant OpenXR implementation.
- Support for the extra 6DOF Dev Kit.
- Support for 3DOF and 6DOF remote controller buttons, trackpad and pose.
- Support for Asynchronous Reprojection to reduce perceived input lag at all times regardless of framerate.
- Correct XRFrameState::predictedDisplayPeriod implementation to improve WebXR render path parallelization.

2. In order to support VR Compositor Layers the following extensions need to be supported in OpenXR SDK:
- https://www.khronos.org/registry/OpenXR/specs/1.0/html/xrspec.html#XR_KHR_android_surface_swapchain
- https://www.khronos.org/registry/OpenXR/specs/1.0/html/xrspec.html#XR_KHR_composition_layer_cube
- https://www.khronos.org/registry/OpenXR/specs/1.0/html/xrspec.html#XR_KHR_composition_layer_equirect2
- https://www.khronos.org/registry/OpenXR/specs/1.0/html/xrspec.html#XR_KHR_composition_layer_cylinder

3. 3D models for the 3DOF and 6DOF controllers to display them in the Reality browser. It should also be added to this repo (https://github.com/immersive-web/webxr-input-profiles/tree/main/packages/assets/profiles) to let WebXR developers load real controller models in any WebXR App.