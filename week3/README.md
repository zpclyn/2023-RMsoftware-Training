# 第3周培训计划(7.3-7.9)

1. 学习`单片机入门`文档并学习工程的建立方法。

3. 完成点灯实验。

``` text
点灯实验
目标：点亮单片机上的LED灯(如果是STM32F1032C8T6，LED对应的引脚为PC13)。
实现：通过调节GPIO输出高低电平驱动LED点亮。（具体原理会在week4进行学习）
```

实验现象：

![](https://github.com/zpclyn/2023-RMsoftware-Training/blob/main/IMAGE/week3/A5ECD25FAE00742097AC1B6C96A2337D.jpg)

参考代码(以STM32F103C8T6为例)：

``` c
#include "stm32f10x.h"                  // Device header

int main(void)
{
	RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOC,ENABLE);//开启GPIOC的时钟
	
	GPIO_InitTypeDef GPIO_InitStructure;//创建GPIO初始化结构体
	GPIO_InitStructure.GPIO_Mode=GPIO_Mode_Out_PP;//配置为推挽输出
	GPIO_InitStructure.GPIO_Pin=GPIO_Pin_13;//配置Pin脚为13
	GPIO_InitStructure.GPIO_Speed=GPIO_Speed_50MHz;//配置GPIO为50MHz
	GPIO_Init(GPIOC,&GPIO_InitStructure);//初始化GPIOC
    	GPIO_ResetBits(GPIOC,GPIO_Pin_13);//配置引脚PC13为低电平
	while(1)
	{
	}
}

```
