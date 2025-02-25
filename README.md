# armbian-linux-6.13-orangepi-5-pro

Self-build armbian image for orangepi-5-pro with linux 6.13 kernel (Armbian does not support 6.13 kernel for opi5pro officially),   
with .dts provided.

Please be noted that this image is **NOT thorougly tested**, use with care.  
Some tested features are as below：  

| feature   | supported | note |
|-------|-----:|:----:|
| hdmi  | ✅ |   only hdmi0 out (the one closer to typeC)  |
| wifi  | ✅ |  could be automatically detected  |
| gpu  | ✅ |  vulkan for mali g610 (yey^^) |
| npu  | ❌ |  not available |
| fan  | ❌ |  somehow it just won't work |
| usb3 | ❌ |  I'm not using it so... :) |
| eth | ❌ | I'm not using it so... :) |

### If you want to build your own

git clone https://github.com/armbian/build.git  
Copy-paste `rk3588s-orangepi-5-pro.dts` to `patch/kernel/archive/rockchip64-6.12/dt/rk3588s-orangepi-5.dts`  
(optinal) Modify `rk3588s-orangepi-5-pro.dts`  
run `./compile.sh build BOARD=orangepi5pro BRANCH=edge KERNEL_GIT=shallow`  




