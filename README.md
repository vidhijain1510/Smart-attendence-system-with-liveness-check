# About my first project on GitHub.
#Introduction\
The Automated Attendance System with Facial Recognition and Liveness Detection is designed to streamline the attendance process in educational institutions. By leveraging advanced technologies such as DeepFace for facial recognition and TensorFlow for liveness detection, the system ensures accurate and efficient attendance tracking while preventing spoofing attacks. Attendance records are seamlessly integrated with Excel, providing a reliable method for record-keeping.

#Objectives\
Automate the attendance marking process.
Ensure the authenticity of individuals using liveness detection.
Maintain accurate attendance records in an Excel sheet.
Provide a user-friendly interface for real-time attendance monitoring.
Technologies Used
DeepFace: For facial recognition.
TensorFlow: For liveness detection to prevent spoofing.
OpenCV: For video capture and image processing.
pygame: For creating a graphical user interface.
keyboard: For detecting key presses.
xlwings: For Excel integration to record attendance.
datetime: For handling date and time data.

#System Design\
Facial Recognition-
The system uses the DeepFace library to recognize faces from the video feed captured by the webcam. Recognized faces are compared against a pre-existing database of student images to identify individuals.
Liveness Detection-
To prevent spoofing attacks, the system incorporates liveness detection using a pre-trained model loaded with TensorFlow. This model distinguishes between a live face and a photograph or video.
Attendance Recording-
Attendance is recorded in an Excel sheet using the xlwings library. Each sheet is named after the current date, and attendance records include the student's name, date, and time of entry.
User Interface-
The user interface is built using pygame, providing a real-time display of recognized faces along with the date and time. Notifications are shown when attendance is successfully recorded or if the student has already been marked present.

#Implementation\
Initialization
Load the pre-trained liveness detection model.
Initialize the Excel workbook and create a new sheet for the current date.
Set up the pygame display and load the background image.
Main Loop
Capture video frames using OpenCV.
Perform facial recognition using DeepFace.
If a face is recognized, extract the coordinates and perform liveness detection.
If the liveness check passes, display the student's name on the screen and wait for the 'enter' key press to record attendance.
Update the Excel sheet with the student's name, date, and time if not already recorded.
Handling New Days
Each new day, a new sheet is created in the Excel workbook.
Reset the list of recorded students and other necessary variables.
Exiting the System
Release the video capture and quit pygame when the program is terminated.
Results
The system successfully recognizes students, verifies their liveness, and accurately records their attendance in an Excel sheet. The graphical interface provides clear real-time feedback, and the integration with xlwings ensures that records are well-maintained and accessible.

#Conclusion\
The Automated Attendance System with Facial Recognition and Liveness Detection offers a robust solution for educational institutions to manage attendance efficiently and securely. By leveraging facial recognition and liveness detection, the system enhances security and reduces manual effort, ensuring that attendance records are accurate and reliable.

This project is a significant step towards modernizing attendance systems in educational settings, providing a seamless and secure way to handle attendance tracking.
