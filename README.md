# Group-Project-
A project done by Justin Centeno for Cis 344 Database class

## First Step
Download both files needed, Appointments.zip and appointments.sql.

## Second Step
Make sure your xampp is up and running and then navigate to PHPMYADMIN on your browser

## Third Step 
Once you login into your PHPMYADMIN page (if login is even needed). Click Import at the top of the page and then under the section File to Import, click browse and select the appointments.sql file.
<img width="1033" height="1295" alt="image" src="https://github.com/user-attachments/assets/4564bc5d-d006-4dca-9f62-f092396495e5" />

## Fourth Step
Next Extract the contents of the Appointments.zip into your htdocs folder. When you extract there should be another folder called Appointments with all the files needed inside 
<img width="674" height="476" alt="image" src="https://github.com/user-attachments/assets/4c421758-ff36-41dd-87cc-aaa28ecf9905" />

## Last Step
Navigate to http://localhost/Appointments/index.php to arrive at the page. You can use index.html, but it will simply redirect you to the php version. <img width="1184" height="1288" alt="image" src="https://github.com/user-attachments/assets/798527b5-ef80-4825-beeb-6e6b4feefeb7" />


### Explainations
The thought process was to have a website that helped you make any appointment based on what type of doctor you needed and what day you wanted it, while also hiding days where the doctor already had an appointment. I worked on it alone, so I had to tone it down immensenly. Now I use simple tables to store the doctors name, and days avaible to help make the appointment. When you make a selection on the first drop down, it affects the second drop down and what days are avaible to make an appointment. Then you fill in your Full name and date birth then create a 4 digit pin. When you click book appointment button it will write to the database, and show a confirmation. Next you will goo to Your Appointments page and fill in whats required to have it display your appointment. It uses the stored doc_id to do a join with the doctors table to display the full name of the doctor you have in your appointment.I wish to finish the website and make it more robust, but i need some free time to rip it apart and start from the bottom up again

### Some Issues Faced
-Had a hard time doing the database properly 
-Getting php to actually write to the database was hard.
-Remembering to hash the password and sanitize inputs

