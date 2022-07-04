# RISC-V Privileged Architecture

## Why a Privlileged Architecture?

* 需要管理共享资源：内存、IO设备、CPU核心

* 需要保护共享资源：

    - 内存：虚拟内存映射

    - IO设备：虚拟内存映射

    - 访问权限：集成在映射中或者作为单独的功能模块

* 需要隐藏实现细节

    - 为软件仿真捕获未实现的操作

    - 处理外部异步事件

        + IO事件、计时器时间、其他线程的软件中断等

    - 用于支持 Hypervisor 的两级地址转换

* 在软件结构栈的各层级之间提供更加清晰的界限拆分

    ![layers](./img/layers.jpg)

    |Layer      |Communicates with          |via                |
    |-----------|---------------------------|-------------------|
    |Application|Application Execution Environment (AEE)|Application Binary Interface (ABI)|
    |Operating System|Supervisor Execution Environment (SEE)|System Binary Interface (ABI)|
    |Hypervisor|Hypervisor Execution Environment (HEE)|Hypervisor Binary Interface (HBI)|

* 用于通信的ECALL指令

* 所有ISA级别设计以支持虚拟化


## Profiles



## Privileges and Models

## Privuleges Features

### CSRs

### Instructions

## Memory Addressing

### Translation

### Protection

## Trap Handling

### Exceptions

### Interrupts

## Counters

### Time

### Performance

