# Ahjizni | احجزني
This project is for **Human-Computer Interaction-IT 215** course, the Supervisor is <br>Dr. Asma Al-Shargabi, and the team members are:<br>
-  Mothla Alnoshan
-  Rawf Alharbi
-  Feda ALnafisah
-  Wajd ALjaber
-  Saja Alsaab
-  Lamees Aloqlan
-  Deem Alorainy


## Introduction to the system
At Qassim University, specifically the College of Computer, we decided to design a smart parking system . The system is complex and works on more than one side, not only a program, but the need for external devices such as sensors, surveillance cameras, QR code readers, and electronic gates to work as an integrated system from all sides, but of course communication with this system is done through the program designated for it.The system is linked to the university’s database, as each of the university’s female members can log in using the university email, password, and mobile number, and thus she can reserve a parking spot through our application. This is to ensure that the owner of the reservation is a member of Qassim University, especially the College of Computer. The system works on displaying the available parking spots, as in the view of a plane or train seats. The member chooses the desired parking spot and reserves it. The system then creates a QR code so that she can log in to the parking lot and also log out after that so that the parking spot is made available to the rest of the university's members. The system supports both languages (Arabic and English).

## Problem Statement
We decide to develop this kind of system because there are many problems arising from the lack of dedicated parking spaces for university female members. Among these problems: being late for official working hours, and parking in places not designated for parking. This may expose the car and its owner to accidents, or the car may be exposed to scratches or damages. The solution may lie in coming early until the member finds a parking spot, but the current parking spots are taken by non-university members, including workers or people from outside the college.
## Objectives
Our goal of this system is to specify university parking lots for university staff and employees by linking this system to the university database, and it also aims to reduce the speed in driving to get a car parking spot and will facilitate and organize this matter, as it will reduce the wrong parking that results in taking more than one parking spot by the member. So we designed this system that solves these problems in all respects.
## Design styles
1. Direct manipulation style.
2. Fill-in style.
3. Standardized task sequences.
4. Descriptive embedded link.

5. Format of displayed information is linked clearly to the format of data entry.
6. Permit easy reversal of actions.
7. Menu selection.
8. Prevent errors.
## How this system will be implemented in the real world?
Our application allows parking reservation service for 4 consecutive periods : <br><br>
**5:00AM-7:30AM**<br> 
**7:30AM-10:00AM**<br> 
**10:00AM-12:00PM**<br>
**12:00PM-2:00PM**<br><br>
Why is that? because if one period of time is allocated for reservation, this will cause the presence of a reserved parking spot without using it for full time, for example, a member who has booked a parking spot at 9 AM, this parking will be available starting from 7 AM, while the member will not come until 9 AM and thus the parking will remain empty until the member comes, on the other hand, there will be members who are required to attend from 7 AM, so she will not find a parking spot for her, so 4 periods have been approved so that each member finds an appropriate spot according to the time of her attendance to the university.<br><br>
When booking, the parking will be available starting from the parking time until half an hour, for example, if the member booked the parking spot at 9 AM, the parking will be available for her from 9 AM until 9:30 AM, after that the parking spot will be canceled. To avoid any damage or accidents that may result from trying to arrive quickly so as not to cancel the parking spot, the member can log in to her account, update the time counter and add 10 minutes, and this update is available only once per reservation. If she did not attend, a message will be sent to the phone number and email registered in the system, that the reservation has been canceled due to the delay in attendance. In the college car parks, electronic gates and a QR code reader are required, as well as a sensor at the entrance and exit entrances. It also requires the presence of sensors in each parking area.<br><br>
**First,** we have the ideal state that we want the system to implement:
When a member reserve a specific parking spot, a QR code will be generated that contains information about the parking area, its number, and the member-assigned ID, as stored in the database.
How is it used? When the member arrives at the university, she will first face the electronic entry portal with a QR code reader and a sensor, the sensor will read the vehicle plate, as she will display the QRCODE on the QR code reader, the reader will store this code after decode it, the system will store the information coming from the sensor and from the reader with each other as one object and store it in the database, we will learn later the importance of this point. After that, the member can enter the parking lot and reach her parking spot using the number and the name of the area as indicated in the reservation details.<br><br>
As we mentioned before, there will be a sensor in each area, this sensor is programmed to specific dimensions of it, which is able to know the dimensions of each parking spot and the name of each one as stored in the database related to it, for example, area A contains two sensors, each one is storing 4 parking spots and the dimensions of each parking, sensor 1 carries data and parking dimensions from A-1 to A-4 and sensor 2 carries from A-5 to A-8 and so on, this sensor will read the vehicle plate and compare it with the database that holds the entry data (when the member enters from the gate) and checks through the code (which the system stored and decode at the gate) and compares the data with the dimensions of the requested parking, if the reserved parking is A-1, the sensor's system will compare the dimensions of the parking A-1 with the spot that the member stands on it, if it matches, there will not be any problems, and this is the ideal case, but if it does not match, then here lies the problem and we will talk about it in the next case. Upon completion and exit, there will be a QR code reader that will read the same entry code to log out and make the parking spot available again.<br><br>

**In the second case,** when the member has reserved a parking spot, but she is parking in another spot that is not hers. The sensor for the area where she stopped will read the vehicle plate and check whether it is in the correct spot or not, if she is in the wrong spot; The system will send a message via her mobile number and e-mail informing her that the place she stopped is wrong and that she must adjust the position. If she does not respond within 10 minutes, an initial warning will be raised to her, and when she reaches 3 warnings; A wrong parking violation will be imposed on her, also in the event that the parking spot in which she was stopped is reserved for another member, the parking spot of the second member will be changed and she will be notified by a message that her parking spot has been updated due to the violation by another member.<br><br>

**In the latter case,** the member stopped in the same spot she reserved, but stopped illegally and obstructed the parking of the other member. In this case, also, a message will be sent to her to notify her, and if she did not respond within 10 minutes, an initial warning will be raised to her, and similarly, if the other spot was reserved for another member before, another spot will be reserved for the second member and she will be informed of this. If it is not reserved, the system will make it
unavailable so that it will not be reserved by other members.

## If you are interested to see our application
[Ahjizni App vedio](https://drive.google.com/drive/folders/1--lzI5Uycd48wb2Zl6emru8vv3EK1vOS?usp=sharing)

 


