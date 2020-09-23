
Most information in this file can be reproduced by running `dump_interrupts(odrv0)` and `dump_dma(odrv0)` in `odrivetool`.

Take this info with a grain of salt as we might forget to update it from time to time. When in doubt check the file history.

# ODrive v3.6

## Interrupt Vectors

 - lowest priority: 15
 - highest priority: 0

|   # | Name                    | Prio |
|-----|-------------------------|------|
| -12 | MemoryManagement_IRQn   |    0 |
| -11 | BusFault_IRQn           |    0 |
| -10 | UsageFault_IRQn         |    0 |
|  -5 | SVCall_IRQn             |    3 |
|  -4 | DebugMonitor_IRQn       |    0 |
|  -2 | PendSV_IRQn             |   15 |
|  -1 | SysTick_IRQn            |   15 |
|   6 | EXTI0_IRQn              |    1 |
|   7 | EXTI1_IRQn              |    1 |
|   8 | EXTI2_IRQn              |    1 |
|   9 | EXTI3_IRQn              |    1 |
|  10 | EXTI4_IRQn              |    1 |
|  11 | DMA1_Stream0_IRQn       |    4 |
|  13 | DMA1_Stream2_IRQn       |   10 |
|  15 | DMA1_Stream4_IRQn       |   10 |
|  16 | DMA1_Stream5_IRQn       |    3 |
|  19 | CAN1_TX_IRQn            |    9 |
|  20 | CAN1_RX0_IRQn           |    9 |
|  21 | CAN1_RX1_IRQn           |    9 |
|  22 | CAN1_SCE_IRQn           |    9 |
|  23 | EXTI9_5_IRQn            |    1 |
|  40 | EXTI15_10_IRQn          |    1 |
|  44 | TIM8_UP_TIM13_IRQn      |    0 |
|  45 | TIM8_TRG_COM_TIM14_IRQn |    6 |
|  50 | TIM5_IRQn               |    1 |
|  52 | UART4_IRQn              |   10 |
|  67 | OTG_FS_IRQn             |    6 |
|  77 | OTG_HS_IRQn (aka ControlLoop_IRQn) |    5 |


## DMA Streams

 - lowest priority: 0
 - highest priority: 3

| Name         | Prio | Channel                          | High Level Func |
|--------------|------|----------------------------------|-----------------|
| DMA1_Stream0 |    1 | 0 (SPI3_RX)                      | SPI             |
| DMA1_Stream2 |    0 | 4 (UART4_RX)                     | UART0           |
| DMA1_Stream4 |    0 | 4 (UART4_TX)                     | UART0           |
| DMA1_Stream5 |    2 | 0 (SPI3_TX)                      | SPI             |
| DMA2_Stream0 |    0 | 0 (ADC1)                         | freerunning ADC |
