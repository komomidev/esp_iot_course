การเรียนรู้ Arduino ESP32 เป็นกระบวนการที่สนุกและท้าทาย เนื่องจาก ESP32 เป็นไมโครคอนโทรลเลอร์ที่มีความสามารถมากมายและใช้งานได้กับหลายแพลตฟอร์มต่าง ๆ ไม่ว่าจะเป็นการพัฒนาโปรแกรมเพื่อ IoT (Internet of Things) หรือโปรเจกต์อิเล็กทรอนิกส์ทั่วไป

ขั้นตอนพื้นฐานสำหรับการเรียนรู้ Arduino ESP32:

1. **เตรียมฮาร์ดแวร์**:
   - มีบอร์ด Arduino ESP32 เช่น NodeMCU-32S, ESP32 Dev Kit, หรือบอร์ด ESP32 อื่น ๆ ตามที่คุณมีอยู่
   - สาย USB เพื่อเชื่อมต่อ ESP32 กับคอมพิวเตอร์

2. **ติดตั้ง Arduino IDE**:
   - ดาวน์โหลดและติดตั้ง Arduino IDE จากเว็บไซต์ของ Arduino (https://www.arduino.cc/en/software)
   - เปิด Arduino IDE และติดตั้งเครื่องมือสำหรับ ESP32 โดยไปที่ **เมนู File > Preferences** และใส่ URL นี้ในช่อง Additional Board Manager URLs:
     ```
     https://dl.espressif.com/dl/package_esp32_index.json
     ```
   - ไปที่ **เมนู Tools > Board > Boards Manager**, ค้นหา "esp32" และติดตั้ง ESP32 by Espressif Systems

3. **เลือกบอร์ด ESP32**:
   - เมื่อติดตั้งเครื่องมือสำหรับ ESP32 เสร็จสิ้น ไปที่ **เมนู Tools > Board** และเลือกบอร์ด ESP32 ที่คุณมี (เช่น NodeMCU-32S)

4. **เรียนรู้การเขียนโค้ด**:
   - เรียนรู้เกี่ยวกับภาษาโปรแกรม Arduino (C/C++) และการใช้งานไลบรารีของ ESP32
   - เริ่มต้นจากโค้ดที่ง่ายๆ เช่นการส่งข้อความไปยัง Serial Monitor หรือการเปิด-ปิด LED

5. **ทดลองโปรเจกต์ต่างๆ**:
   - ทดลองโปรเจกต์ง่ายๆ เพื่อเรียนรู้การใช้งาน ESP32 ได้แก่:
     - การควบคุม LED ด้วยสวิตช์หรือแสดงผลตามเซ็นเซอร์
     - การส่งข้อมูลไปยังเว็บเซิร์ฟเวอร์ผ่าน Wi-Fi
     - การใช้งาน Bluetooth หรือการสื่อสารแบบไร้สาย

6. **การเรียนรู้เพิ่มเติม**:
   - อ่านเอกสารและคู่มือการใช้งาน ESP32 จากเว็บไซต์ของ Espressif Systems
   - เรียนรู้จากชุมชน Arduino ESP32 บนเว็บไซต์ต่าง ๆ เช่น GitHub, Arduino Forum, และช่อง YouTube

7. **ทดลองโปรเจกต์ IoT**:
   - ลองสร้างโปรเจกต์ IoT ง่ายๆ เช่นระบบส่งข้อมูลเซ็นเซอร์ไปยังแพลตฟอร์ม IoT (เช่น ThingSpeak, Blynk)

8. **การปรับแต่งและพัฒนา**:
   - ศึกษาเพิ่มเติมเกี่ยวกับการใช้งานหลายๆ ฟีเจอร์ของ ESP32 เช่นการใช้งาน GPIO, การเชื่อมต่อกับอุปกรณ์อื่น ๆ ผ่าน SPI, I2C, UART และอื่น ๆ
   - พัฒนาโปรเจกต์ที่น่าสนใจเพื่อศึกษาและปรับปรุงทักษะการเขียนโปรแกรม

การเรียนรู้ Arduino ESP32 เป็นการเรียนรู้ที่มีประสิทธิภาพมากในการศึกษาการเขียนโปรแกรมในรูปแบบของ IoT และอิเล็กทรอนิกส์ และยังเป็นพื้นฐานที่ดีสำหรับการศึกษาเกี่ยวกับการทำงานของไมโครคอนโทรลเลอร์ในรูปแบบพื้นฐานและขั้นสูง

# เตรียมเครื่องสำหรับพัฒนา IoT

ก่อนการพัฒนา IoT จะต้องทำการติดตั้ง โปรแกรม สำหรับสร้าง Environment สำหรับการพัฒนาโปรแกรมด้าน IoT

##  1. Chocolatey  
Chocolatey เป็นเครื่องมือการจัดการซอฟต์แวร์ package management แบบฟรีสำหรับ Windows เราสร้างติดตั้งโปรแกรมต่างผ่านทาง Repository ของ Chocolatey  <https://chocolatey.org/install>

![chocolate](../assets/images/chocolatey1.png)

เปิด Powershell ด้วยสิทธิ Administrator

```sh
> Set-ExecutionPolicy AllSigned

> Set-ExecutionPolicy Bypass -Scope Process

> Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

```
ตัวอย่างหน้าจอ
![ps_chocolatey](../assets/images/ps_chocolatey.png)

Reboot เครื่อง  หลังจากนั้น ให้ทำการติดตั้ง package จาก Powershell ดังนี้
- rsync
- wget
- python
- nodejs
- make

```sh
> choco install rsync wget python nodejs
> choco install make
```

ตัวอย่างหน้าจอ
![choco_install](../assets/images/choco_install.png)

## 2. Arduino IDE 2

Arduino IDE เป็น Editor สำหรับการพัฒนาโปรแกรม ด้วย Arduino Framework
<https://www.arduino.cc/en/software>  และ Download MSI installer 

![arduino_download](../assets/images/arduino_download.png)

กด Just Download

![just_download](../assets/images/just_download.png)

ดำเนินการติดตั้ง โปรแกรมแบบ ปรกติ
![arduino_install_1](../assets/images/arduino_install_1.png)

เปิดโปรแกรม Arduino IDE และ ไปยัง เมนู File > Preferences เพื่อทำการตั้งค่า
![arduino_install_2](../assets/images/arduino_install_2.png)


เพิ่มเติม บอร์ด ESP32 ให้แก่ Arduino IDE เพื่อให้สามารถใช้ สามารถพัฒนา iot ร่วมกับ ESP32 บอร์ดได้
![arduino_install_3](../assets/images/arduino_install_3.png)

เพิ่ม link Additional Boards Managers
```
https://espressif.github.io/arduino-esp32/package_esp32_index.json
```
```admonish
Ref อ้างอิง Code สำหรับ ESP32 Core Arduino  <https://github.com/espressif/arduino-esp32>
```

### ข้อมูลสำหรับ บอร์ด ตระกูล ESP32 
| **SoC**  | **Stable** | **Development** |                                           **Datasheet**                                           |
|----------|:----------:|:---------------:|:-------------------------------------------------------------------------------------------------:|
| ESP32    |     Yes    |       Yes       |    [ESP32](https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf)    |
| ESP32-S2 |     Yes    |       Yes       | [ESP32-S2](https://www.espressif.com/sites/default/files/documentation/esp32-s2_datasheet_en.pdf) |
| ESP32-C3 |     Yes    |       Yes       | [ESP32-C3](https://www.espressif.com/sites/default/files/documentation/esp32-c3_datasheet_en.pdf) |
| ESP32-S3 |     Yes    |       Yes       | [ESP32-S3](https://www.espressif.com/sites/default/files/documentation/esp32-s3_datasheet_en.pdf) |
| ESP32-C6 |     No     |       Yes       | [ESP32-C6](https://www.espressif.com/sites/default/files/documentation/esp32-c6_datasheet_en.pdf) |
| ESP32-H2 |     No     |       Yes       | [ESP32-H2](https://www.espressif.com/sites/default/files/documentation/esp32-h2_datasheet_en.pdf) |


<https://products.espressif.com/#/product-comparison>

## อ้างอิง
[ดูข้อมูลเปรียบเทียบ](./ref/compare_esp1.md)

![Esp32-DevKit-V1-Pinout(PNG)](../assets/images/ESP32-DevKit-V1-Pinout-Diagram.png)