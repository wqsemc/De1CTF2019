出这个类型的题，主要是考察选手对加密固件的提取，题目涉及的是DIR-850L固件的真实加解密，也是希望选手在做了题之后有所收获，能够在真实设备上做进一步的漏洞挖掘

这道题有两个预期解，一是直接通过逆向升级的部分编写解密脚本，加密不是很难，已给出了AES所需的key，对设备有一些研究的在看了这个cgi-bin之后通常都能猜到是哪些型号，所以我patch掉了一些信息；二是巧解，在固件升级的过程中他可以直接调用解密程序对固件解密，所以需要qemu运行一个同架构的虚拟机，然后调用解密程序解出来