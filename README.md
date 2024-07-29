# aleopool aleo_worker
##  介绍
- 矿池挖矿
- 挖矿前准
- 接入池子
## 矿池挖矿
您需要在矿池 (http://8.218.31.102:8080/register) 注册一个账户账户，同时还需要进行以下操作：
#### 
                
1. 设置谷歌验证
2. 查找account与设置收益地址  
    account：登录账号->点击右上角账号->设置   
    地址设置：登录账号->点击右上角账号->设置->安全设置->谷歌验证的开放->挖矿账户->设置(付款设置下)         
    Aleo钱包可以在 tools.aleo1.to 或aleo.tools上生成。
## 挖矿前准备
挖矿设备：GPU（NVIDIA显卡，显存不低于6GB，显卡驱动版本550或以上）。推荐每个GPU配备8核CPU（如2个GPU则配备16核CPU），以及8G内存（2个GPU则配备16G内存），128G固态硬盘。

操作系统：安装系统版本Ubuntu 22.04，server版，不带GUI组件。  

需要 Nvidia 525 驱动程序和 CUDA 12 才能获得最佳性能。
您可以在此处找到说明：https://developer.nvidia.com/cuda-downloads  
矿工 GPU 负载过重 - 检查您的电源单元和 PL 设置。矿工启动后 - 在前 30-60 分钟内观察 GPU 和 CPU 的温度。如果过热 - 降低 PL，调整 OC。

## 接入池子
下载二进制文件:  
`wget -O jlaleo-v0.0.1.tar.gz  https://github.com/jilingtech/client/releases/download/v1.0.1/jlaleo-v0.0.1.tar.gz
`
提取文件:  
`tar -zxvf jlaleo-v0.0.1.tar.gz `  
接入命令：  
`./jl-aleo-prover  --url ws://116.117.158.178:18888/v1/api/client/ws --account 55138c1ab035b540  --worker worker1 --threads 95`  
```
--account - 账号ID  
--url - pool地址  
--worker - 矿工名称  
--threads - 线程数
```

