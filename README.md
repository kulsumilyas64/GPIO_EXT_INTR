## Code for Toggling LED 2 on Board by External Interrupt 

```
#include"main.h"

void HAL_GPIO_EXTI_Callback(uint16_t GPIO_Pin)        // External Interrupt Call Back on GPIO PIN
{
	if (GPIO_Pin == B1_Pin){                            // B1 - Blue pin on the Board
		HAL_GPIO_TogglePin (LD2_GPIO_Port, LD2_Pin);      // Toggling Function
	}
	else{
		__NOP ();
	}
}

```
