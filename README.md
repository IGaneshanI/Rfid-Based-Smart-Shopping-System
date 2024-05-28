Default the system only have one Admin only
USERNAME:: Admin
PASSWORD:: Admin123



All the details of user are stored onto database into table userinformation which is encrypted
All the RFID and product details are stored into rfid_info table and all the data here is also encrypted

Run Home.java file
Requirement
Softwares:
WAMP/XAMP/LAMP for MYSQL database
Netbeans/IntelIJ for development purpose
JAVA 1.8 (JDK 1.8 & JRE 1.8)

Hardware:
Arduino UNO r3(2 piece)
RC522 RFID scanner module
Buzzer, LED's (2 RED AND 2 GREEN), Jumper Cables,

Setup:
Download the zip file and extract all the folder's from it.

Keep this extracted folder named "RFID_Based_SmartShoppingSystem" in 'C://' only which look like "C://RFID_Based_SmartShoppingSystem/" to avoid errors.

Import the SQL file named "rfid_basedshoppingsystem" to your Database. You can see how to import the sql file in WAMP/XAMP/LAMP from youtube.

Upload the arduino file named "RFID.ino" in one of the Arduino UNO from "/arduino files/RFID/RFID.ino"
Upload the another file named "Exit.ino" in another Arduino UNO form "/arduino files/Exit/Exit.ino".

Attach those 2 Arduino boards to your system and See the circuit diagram for connection reference given in "Smart shopping System final.pptm" on slide #5 & #6 and "Smart shopping system final.pdf" on page #24.

The jar files required by you are in folder named "jarfiles". You can see how to add jar files to your project from youtube.

Note: Avoid Changing Directory Structure provided to you and follow all setup steps thouroly;
Contains To be Modified Before running:
In DBConnection.java
line: 23 -> Enter the servername of your DB in place of "servername", Enter the port_number of your DB in place of "port_number", Enter User name and Password in place of "User_Name here" & "Password here" respectively connection = DriverManager.getConnection("jdbc:mysql://servername:port_number/rfid_basedshoppingsystem?useSSL=false", "User_Name here", "Password here");

In Email.java
line: 114-> Enter sender's email in place of "your_email@gmail.com" in String user = "your_email@gmail.com";

line: 115-> Enter sender's account's password in place of "your password" in String pss = "your password";

line: 154 -> Enter reciever's email in place of "To_email_address"

In Email_Bill.java
line: 92 -> Enter sender's email in place of "your_email@gmail.com" in String user = "your_email@gmail.com";

line: 93 -> Enter sender's account's password in place of "your password" in String pss = "your password";

line: 147-> Enter reciever's email in place of "To_email_address" and Pdf file path in place of "C:\RFID_Based_SmartShoppingSystem\pdfFiles\@kevin.pdf" in sendMessage("To_email_address","C:\RFID_Based_SmartShoppingSystem\pdfFiles\@kevin.pdf");

In Java2arduino.java
line: 14 -> Check the your COM port of arduino connected to Arduino with LED's and enter here appropriate one in place of "COM4" in Arduino("COM4", 9600);

In Arduino2java.java
line: 76 -> Check the your COM port of arduino connected to Arduino with RC522 module and enter here appropriate one in place of "COM3" in System.setProperty("gnu.io.rxtx.SerialPorts", "COM3");
