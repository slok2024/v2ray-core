# v2ray for win7

对v2ray 源码通过go1.25.7 for win7魔改版进行重新编译，性能和安全进一步提升。同时编译i386及amd64 v1到v4多个版本，并使用upx进行压缩以减少体积。

可根据自己电脑处理器来下载对应内核到软件安装目录进行替换即可，让代理软件发挥最大性能。


处理器支持情况详细划分

GOAMD64=v1  (基础版)
支持： 只要是 64 位 CPU 就能跑。
代表：甚至包括老旧的奔腾、赛扬 64 位处理器。

GOAMD64=v2  (平衡版)
Intel: Core i7/i5/i3 (Nehalem 及以后)，即一代酷睿之后的所有产品。
AMD: Opteron, Phenom II, FX 系列 (Bulldozer架构)。

GOAMD64=v3  (性能版)
Intel: 第 4 代 Haswell (如 i7-4770) 及以后的所有酷睿处理器。
AMD: Ryzen (所有系列)，以及 Excavator 架构及以后的 APU。
优势：增加了 AVX2，这对于处理加解密数据流和哈希表匹配有显著加速作用。

GOAMD64=v4  (极限版)
Intel: 第 11 代以后（部分型号禁用了 AVX-512）、至强 (Skylake-SP 及以后)。
AMD: Ryzen 7000 系列 (Zen 4) 及以后。
注意：如果 CPU 不支持 AVX-512，运行 v4 编译的程序会直接报 Illegal Instruction 错误导致崩溃。
