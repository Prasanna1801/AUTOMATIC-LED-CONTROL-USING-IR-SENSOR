# AUTOMATIC-LED-CONTROL-USING-IR-SENSOR
##  AIM
To design and implement a system using the **STM32 microcontroller** where an LED automatically turns ON or OFF based on the input from an **IR sensor**.

---

##  Components Required
- STM32 Nucleo or Discovery Board (e.g., **Nucleo-G071RB**)
- IR Sensor Module
- LED (5mm Green or any color)
- Jumper wires
- Breadboard

---

##  Theory
An **IR sensor** detects the presence of an object by emitting and receiving infrared light.

### IR Sensor Behavior
- When an **object is detected**, the IR sensor output goes **LOW (0V)**.
- When **no object is detected**, the output stays **HIGH (3.3V)**.

### Microcontroller Response
- If **IR output = LOW** → **LED ON**
- If **IR output = HIGH** → **LED OFF**
### **Procedure**

1. Open **STM32CubeIDE**.
<img width="1920" height="1200" alt="Screenshot 2025-10-28 110943" src="https://github.com/user-attachments/assets/02b5bdbc-7f1c-42fb-a393-e64cd3533fda" />


2. Click **File → New STM32 Project**.
   <img width="1920" height="1200" alt="Screenshot 2025-10-28 111302" src="https://github.com/user-attachments/assets/e9ec3c5d-c6c5-472c-8100-964009fdfdbe" />

3. Select the **target microcontroller** or board and click **Next**.
   <img width="1920" height="1200" alt="Screenshot 2025-10-28 111618" src="https://github.com/user-attachments/assets/87d6c9c7-8781-4877-9832-f76e8f5594c4" />


4. Name the project.
   <img width="534" height="596" alt="Screenshot 2025-10-28 111703" src="https://github.com/user-attachments/assets/a96fe9ff-eef2-43d5-875c-e368d93b8252" />

5. The corresponding `.ioc` file will be generated automatically.
   <img width="1920" height="1200" alt="Screenshot 2025-10-29 152608" src="https://github.com/user-attachments/assets/39196d5e-dc9a-4f09-be72-f26a2991d5d3" />

6. Configure the pins as **GPIO (Input/Output)**, **USART**, etc. as needed.
  <img width="1920" height="1200" alt="Screenshot 2025-10-29 153109" src="https://github.com/user-attachments/assets/cd97c1e1-fb32-44b7-959d-52329c691c5a" />

7. Save the configuration (`Ctrl + S`) – the base C program will be generated automatically.
   <img width="1080" height="608" alt="image" src="https://github.com/user-attachments/assets/dbf4b205-5db9-4e9b-8150-94f441c8b116" />
 
8. Edit the generated main program as required.
<img width="1308" height="1159" alt="image" src="https://github.com/user-attachments/assets/63a1c7c3-f078-4436-988f-f599e6b4b71c" />

9. Click **Project → Build All**.
    <img width="1920" height="1200" alt="Screenshot 2025-10-29 155619" src="https://github.com/user-attachments/assets/9ed11033-6c66-4594-969d-fbf1b1df68be" />

10. Link the **HEX file** using the post-build process.
    <img width="624" height="397" alt="Screenshot 2025-10-29 155720" src="https://github.com/user-attachments/assets/a5536388-e7b8-433a-b79a-c151af89b610" />

11. Click **Debug** and connect the **STM Nucleo Board**.
    <img width="1920" height="1200" alt="Screenshot 2025-10-29 160534" src="https://github.com/user-attachments/assets/232a65bd-5dab-45f6-8af6-aba96b383d02" />


13. Click **Run** to execute the program.
    
---

### 💻 **Program**


```c
#include "main.h"

void SystemClock_Config(void);
static void MX_GPIO_Init(void);

int main(void)
{
    HAL_Init();
    SystemClock_Config();
    MX_GPIO_Init();

    while (1)
    {
        GPIO_PinState ir = HAL_GPIO_ReadPin(GPIOA, GPIO_PIN_10); // IR OUT at PA10 (D2)

	      if (ir == GPIO_PIN_RESET)  // IR sensor HIGH = object detected
	      {
	          HAL_GPIO_WritePin(GPIOB, GPIO_PIN_3, GPIO_PIN_SET); // Turn ON LED
	      }
	      else
	      {
	          HAL_GPIO_WritePin(GPIOB, GPIO_PIN_3, GPIO_PIN_RESET); // Turn OFF LED
	      }

	      HAL_Delay(100);
    }
}
```
---
### OUTPUT
CASE 1: LED ON 
![IMG-20251030-WA0011 1](https://github.com/user-attachments/assets/66a426de-f676-422f-af78-9fc1f28ee4ae)

CASE 2: LED OFF
![IMG-20251029-WA0021 1](https://github.com/user-attachments/assets/cb900a9d-4921-47ba-8876-30c23a740d4d)


---
### RESULT

The experiment on IR Sensor-Based Automatic LED Control using STM32 was successfully carried out. The STM32 microcontroller accurately read the IR sensor output and controlled the LED based on object detection. When an object was detected, the LED glowed (ON) and when no object was present, the LED remained OFF. Thus, the objective of the experiment was achieved.




