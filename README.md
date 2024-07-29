# Aleopool aleo_worker
##  INTRODUCTION
- Aleopool pool mining
- Pre mining preparation
- Access Aleopool Pool
## Aleopool pool mining
You can either register an account on http://8.218.31.102:8080/register ，at the same time, the following operations need to be performed：
#### 
                
1. Google authentication
    login->account->Settings->Security settings->Google authentication
2. look for account and settings address
    account：login->account->Settings->Mining account   
    Settings address：login->account->Settings->Mining account-> Settings/Modify         
    Aleo wallet can be generated at tools.aleo1.to or aleo.tools
## Pre mining preparation
Mining equipment: GPU (NVIDIA graphics card, graphics memory not less than 6GB, graphics card driver version 550 or above). It is recommended to equip each GPU with an 8-core CPU (16 cores for 2 GPUs), 8GB of memory (16GB for 2 GPUs), and a 128GB solid-state drive.

Operating system: Install system version Ubuntu 22.04, server version, without GUI components.

Nvidia 525 drivers and CUDA 12 required for best performance.
You can find instructions here: https://developer.nvidia.com/cuda-downloads
Miner load GPU heavily - check your power unit and PL settings.                                                                After miner starts - watch for temperature of GPU and CPU during first 30-60 minutes. In case of overheating - lower PL, tune OC.

## Access Aleopool Pool
Download binaries:  

```wget -O jlaleo-v0.0.1.tar.gz  https://github.com/jilingtech/client/releases/download/v1.0.1/jlaleo-v0.0.1.tar.gz```  

Extract files for client: 

```tar -zxvf jlaleo-v0.0.1.tar.gz ```  

Usage：  

```./jl-aleo-prover  --url ws://116.117.158.178:18888/v1/api/client/ws --account 55138c1ab035b540  --worker worker1 --threads 95 ```   
```
--account -account ID  
--url     -pool address  
--worker  -workername  
--threads -threads
```

