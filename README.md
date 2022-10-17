# EXPERIMENT NO 05 INTERFACING ANALOG OUTPUT SERVO MOTOR WITH ARDUINO

### AIM
To interface an Analog output (servo motor) and modify the angular displacement of the servo using PWM signal .
COMPONENTS REQUIRED:
1.	Servo motor of choice (9v is preferred )
2.	1 KΩ resistor 
3.	Arduino Uno 
4.	USB Interfacing cable 
5.	Connecting wires 
6.	Servo rated power supply (dc source )


### THEORY
Servo motors and are constructed out of basic DC motors, by adding:
•	 gear reduction
•	 a position sensor for the motor shaft
•	 an electronic circuit that controls the motor's operation
Typically, a potentiometer (variable resistor) measures the position of the output shaft at all times so the controller can accurately place and maintain its setting.
Servo motors are used for angular positioning, such as in radio control airplanes.  They typically have a movement range of 180 deg but can go up to 210 deg.The output shaft of a servo does not rotate freely, but rather is made to seek a particular angular position under electronic control. 


![image](https://user-images.githubusercontent.com/36288975/163544439-1f477927-fcd4-42f0-9ce4-c863fdbf1210.png)



#### Figure-01 SERVO MOTOR SPLIT VIEW 
Control 
An external controller (such as the Arduino) tells the servo where to go with a signal know as pulse proportional modulation (PPM) or pulse code modulation (which is often confused with pulse width modulation, PWM). PWM uses 1 to 2ms out of a 20ms time period to encode its information.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/163544482-3027136f-7135-4f3d-a23f-8dc2fe04194d.png)

### Figure-02 SERVO MOTOR PINS

 ![image](https://user-images.githubusercontent.com/36288975/163544513-ca497421-e6ba-4f91-871f-5cfba77f22a8.png)


### Figure-03 SERVO MOTOR OVERVIEW 

 


 





CIRCUIT DIAGRAM
 
 
 ![image](https://user-images.githubusercontent.com/36288975/163544618-6eb8a7b5-7f1a-428a-8d9f-fd899b145efb.png)

### FIGURE 04 CIRCUIT DIAGRAM

### PROCEDURE:
1.	Connect the circuit as per the circuit diagram 
2.	Connect the board to your computer via the USB cable.
3.	If needed, install the drivers.
4.	Launch the Arduino IDE.
5.	Select your board (If you the board is arduino uno, select accordingly).
6.	Select your serial port, accordingly ( E.g. COM5 )
7.	Open the file of the program  and verify the error , clear if any errors that are existing 
8.	Upload the program and check for the physical working. 
9.	Ensure safety before powering up the device.


### PROGRAM :
```
#Name: Silambarsan K
#Roll No: 212221230101


#include<Servo.h>
Servo s1;
void setup()
{
  s1.attach(9);
}
void loop()
{
  for(int i=0;i<=100;i+=1)
  {s1.write(120);
  delay(15);
}
  for(int i=100; i>=0;i-=1)
  {
    s1.write(i);
    delay(15);
}
}


```
### OUTPUT:
#### circuit OFF setup
![R1](https://user-images.githubusercontent.com/94525786/196165940-2b99ef73-9aad-4e4f-a867-bf6a1f71a757.png)

#### circuit ON setup
![R2](https://user-images.githubusercontent.com/94525786/196165968-1c74a749-18b8-46ac-af2d-0df5b8857354.png

#### Serial monitor:
![3](https://user-images.githubusercontent.com/94525786/196166447-77737a58-06e7-434a-a84b-f27b89516b36.png)

#### Toggle graph:
![4](https://user-images.githubusercontent.com/94525786/196166465-541a692a-2bce-4634-b0c9-c184180c0cf0.png)

### RESULTS: 
Arduino uno interfacing with servo motor is learned and angular position is controlled using PWM signal.

