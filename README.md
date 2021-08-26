# Let's Proctor 

## Aim 

To make a Screen Lock using Python (OpenCV and Tkinter).

![](https://cliply.co/wp-content/uploads/2019/03/371903161_BLINKING_EYE_400px.gif)


## About Application

This Application is made mainly using Python and OpenCV. Its extremely simple and easy to use application that can be very useful for teachers who wish to monitor students during exam. Here is a PDF link on how to use the app. http://letsproctor.herokuapp.com/info 

## Problem it solves
![](https://c.tenor.com/AKS0zwKDvMcAAAAd/mr-bean-exams.gif)

Currently due to lockdown scenario all exams are being held online. This exams are extremely difficult to be monitored and cheating is rampant. To solve this I have created a Application that can be used by Teachers to monitor students. Its simple and easy to use. Teachers have to provide a Google form link (I have purposely used that because teachers mostly use it) and App will send a Unique id to their email and also will be shown on screen. Then student has to download the tool and give all details including the unique id and start exam. After completion teacher can see the results in form of table. App will also provide screenshots since there are chances of false positive.


## Setup instructions / Requirements
For Teachers: Just a browser (Can be done from mobile to :))

For Students:
Install Python 3.7 +
Use Windows OS (exe works on windows only)

## Work Flow / Logic

- For Web part I have used HTML and CSS for frontend and Flask for backend.
- I have used Mongodb (pymongo) as database to store the entries of user.
- When User enters their detail of creating a test, I save all the details in database and create a unique id using uuid tool.
- This unique id is important and plays a major role in connecting student entries with the teacher's.
- Now in proctor.py file there are multiple things included. All the logic behind proctoring is declared there
- Lets go step by step
-   For Gaze detection I am using facemesh of mediapipe library and picking out both the eyes as ROI.
-   After doing that I am checking 4 pixels at some distance
-   If just one of the 4 pixels are black we can say that user has moved his eyes to one side and thus we can count it as violation ![](https://i.ibb.co/th4pb7r/image.png)
-   Then Next comes Face Detection. Again I am using mediapipe but a different solution which is face detect. Its pretty straight forward and in this we are getting points and calculating distances to check if head is tilted or not. Same solution is being used to detect whether face is present or not. Also if multiple faces are present ![](https://i.ibb.co/Ln9YXZG/image.png) 
-   

## Output

Check Out this Youtube Video for Demo https://www.youtube.com/watch?v=PjGLWq3LrhM&ab_channel=TusharAmdoskar
![](https://github.com/TusharAMD/Awesome_Python_Scripts/blob/issue254/GUIScripts/Face%20Lock%20OpenCV/Images/ImagesForReadme/Img1.png)
![](https://github.com/TusharAMD/Awesome_Python_Scripts/blob/issue254/GUIScripts/Face%20Lock%20OpenCV/Images/ImagesForReadme/Img2.png)
![](https://github.com/TusharAMD/Awesome_Python_Scripts/blob/issue254/GUIScripts/Face%20Lock%20OpenCV/Images/ImagesForReadme/Img3.png)

## Author(s)

Tushar Vaman Amdoskar

Find me on Linkedin : https://www.linkedin.com/in/tushar-amdoskar/

## Disclaimers, if any

This script is specifically designed for Windows operating system and will certainly not work on Linux or Unix systems. 
