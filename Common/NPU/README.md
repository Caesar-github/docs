## RK356X/RK3588 RKNN SDK to V1.2.0

### 主要修改

- RK3588支持feature map内存共享，在特定模式下可以节省内存占用

- RK3588支持多batch多核模式，可以更好的发挥NPU多核的性能

- 增加更多OP支持，比如Where, Resize, Pad, Reshape, Transpose等

- 增加调试信息：方便用户定位耗时比较多的OP以及是否DDR等瓶颈

- 修复一些已知的BUG

###  版本号查询

- librknnrt runtime版本：1.3.0（strings librknnrt.so | grep version | grep lib）

- rknpu driver版本：0.7.2（dmesg | grep rknpu）

### 其他说明

- rknn-toolkit适用RV1109/RV1126/RK1808/RK3399Pro，rknn-toolkit2适用RK356X/RK3588

- rknn-toolkit2与rknn-toolkit API接口基本保持一致，用户不需要太多修改（rknn.config()部分参数有删减）

- rknpu2需要与rknn-toolkit2同步升级到1.3.0的版本。之前客户使用rknn toolkit2 1.2.0版本生成的rknn模型建议重新生成**

