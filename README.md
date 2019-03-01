# ปลั๊กอิน BH1750 สำหรับ kidbright

BH 1750 เป็นเซนเซอร์ที่ใช้วัดความเข้มของแสงความละเอียดสูง สามารถสื่อสารข้อมูลด้วย i2c ในการรับส่งข้อมูลระหว่างบอร์ด kidbright

## รายละเอียดอุปกรณ์

* เชื่อมต่อแบบ I2C (มีขา SCL และ SDA)
* ใช้งานและเชื่อมต่อแบบ I2C slave device
* ความเร็วสำหรับบัส I2C ได้ถึง 400kHz
* มีขา ADDR สำหรับต่อกับ LOW หรือ HIGH เพื่อใช้กำหนดเลขที่อยู่ของ I2C Slave (สามารถกำหนดเลขที่อยู่ได้สองค่า)
* แรงดันไฟเลี้ยงในช่วง 2.4V - 3.6V
* เลือกโหมดการวัดได้ (Measurement Mode) เช่น H-resolution Mode, H-resolution Mode2, L-resolution Mode ซึ่งเป็นตัวกำหนดความละเอียดในการวัด รวมถึงระยะเวลาในการวัดและอ่านค่า (measurement time)
* ความละเอียด: 16 บิต ได้ค่า 1-65536 หน่วยเป็น Lux (step: 0.5 Lux, 1 Lux, หรือ 4 Lux ขึ้นอยู่กับโหมดการวัดที่เลือก)
* ระยะเวลาในการวัดแต่ละครั้ง: ประมาณ 120 msec (สำหรับ 0.5 Lux หรือ 1 Lux), 16 msec (สำหรับ 4 Lux) ขึ้นอยู่กับโหมดการวัดที่เลือก

ข้อดีของไอซีตัวนี้คือ ให้ค่าเป็นดิจิทัล ความละเอียดสูงถึง 16 บิต เชื่อมต่อแบบ I2C bus ทำให้ประหยัดจำนวนสัญญาณเชื่อมต่อ ให้ค่าในการวัดเป็นหน่วย Lux ("ลักซ์") ซึ่งเป็นหน่วยการวัดแบบ SI สำหรับความสว่าง (illuminance) = 1 lumen per square meter

### การติดตั้ง

เมื่อดาวน์โหลดไฟล์แล้วให้นำไปใส่ในไดเรคทอรี plugins ของ kidbright
```
C:\\Users\username\AppData\Local\Kidbright\app-1.0.0\resources\app/kbide\plugins\weather_sensors\bh1750
```
## ผู้เขียน

* **Suphanut Thanyaboon** ชมรมเมกเกอร์เมืองหลวง  - *ผู้ริเริ่ม* - [maskung](https://github.com/maskung)

## License

This project is licensed under the MIT License
