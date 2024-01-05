## Description
This demo project evaluates the triangle wave generation capability of the STM32L073RZ:
* A triangle wave is generated through the DAC1 output with its frequency selected by the user button.
* The DAC samples are triggered using TIM6. The frequency is changed by seting __HAL_TIM_SET_PRESCALER or __HAL_TIM_SET_AUTORELOAD on user button interrupt.
* The user led is toggled periodically and messages are sent through USART2 at 115200 bauds in the main loop.

Note: In addition to the triangle wave generator, the DAC features an LFSR white noise generator which can be used by toggling it in the DAC settings (use HAL_DACEx_NoiseWaveGenerate instead of HAL_DACEx_TriangleWaveGenerate).

## Usage
Connect a volume adjust potentiometer, decoupling capacitor, and audio amplifier to DAC1 output (PA4) to listen the generated tones.

## References
Nucleo-64 board user manual: 
https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf

AN3126 Application note - Audio and waveform generation using the DAC  in STM32 products
https://www.st.com/resource/en/application_note/an3126-audio-and-waveform-generation-using-the-dac-in-stm32-products-stmicroelectronics.pdf

