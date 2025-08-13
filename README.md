# 📘 Esoft Practicals Reservation System

### 🔹 Project Name: `Esoft-Practicals-Reservation-System`

---

## 📝 Description

**Esoft Practicals Reservation System** is a desktop application currently in use at **Esoft Piliyandala**.  
It allows students to **book a practical session** by choosing a convenient **date** and **time**, and reserve a **computer (PC)** for their individual session.

This system ensures organized scheduling and avoids conflicts in lab availability, streamlining the practical teaching process.

---

## 🛠️ Built With

- **Programming Language**: C#
- **Platform**: Windows Desktop Application
- **Framework**: .NET Framework
- **Database**: SQL Server / LocalDB
- **Third-party Tools**: Guna UI2 (for modern UI design)

---

## 💾 Installation Guide

Follow these steps to install the system:

1. **Download** the folder named `Esoft Practicals Reservation`.
2. Open the `Esoft Practicals Reservation` folder.
3. Go inside the `Debug` folder located within it.
4. Double-click on the file named `EsoftPracticalsReservation.msi`.
5. On the welcome screen, click **Next**.
6. Browse and select the location where you want to install the software.
7. Click **Next** to proceed.
8. Confirm the installation by clicking **Next** again.
9. Wait until the installation completes.


### 📂 After Installation

The system will be installed in the following directory:

C:\Program Files (x86)\Methum Minsuka\EsoftPracticalsReservation\

Inside this folder, you'll find the following two important files:

- `Database.mdf`
- `Database_log.ldf`

### 🔐 Granting Database Permissions

To ensure the system works correctly with the database, follow these steps:

1. **Right-click** on each of the following files:
   - `Database.mdf`
   - `Database_log.ldf`

2. Select **Properties**.

3. Go to the **Security** tab.

4. Click the **Edit** button under:
   > “To change permissions, click Edit”

5. In the list of user groups, select each of the following and provide **Full control** access:

   - `ALL APPLICATION PACKAGES`
   - `ALL RESTRICTED APPLICATION PACKAGES`
   - `Users (YourPCName\Users)`

6. After granting **Full control** to all, click **Apply**, then **OK**.

7. You can now open the system using the **desktop shortcut** that was created during installation.

![Desktop Shortcut](https://drive.google.com/uc?export=view&id=1cHFkJ6lQvIBZ9m7ILFe3Tn0pEsIMJieX)

---

## ✅ Features

The system offers two main sets of features:

- 🔒 **Admin Features**
- 👤 **User Features**

## 🔒 Admin Features

1. **Secure Login Access**

![Admin Login Page](https://drive.google.com/uc?export=view&id=1XM-mfd-m4Lg9QCXpyVVYu63QuHfbh9-Z)

Enter the **Admin Password** into the text box and click the **Admin Login** button.  
If the password is correct, you will be redirected to the **Admin Panel**.

2. **View Reservations**

![Admin View Reservations](https://drive.google.com/uc?export=view&id=1HfcvYV_M15EaCkWNEueLS4AaK7o8o7S1)

Admins can view all reservation records submitted by students.

Admins can also **filter** reservations based on:

- ✅ Specific date range (From – To)
- 🆔 Student Registration Number
- 🔢 Batch Code
- 🏷️ Course Category
- 🕐 Reserved time slot
- 🚪 Attendance status (Whether the student actually attended or not)

> ✅ This allows for detailed tracking, monitoring, and reporting of student practical sessions.

3. **View Registered Users**  

![Admin View Registered Users](https://drive.google.com/uc?export=view&id=1d20-rqgkj5RuZeUy1YPbEKOVbj-bjJYv)

Admins can view a complete list of all registered students within the system.

Additionally, the list can be **filtered** using the following criteria:

- 🆔 Registration Number  
- 🧍 First Name  
- 🧍‍♂️ Last Name  
- 🔢 Batch Code  
- 🏷️ Course Category  

#### ✏️ Update or Delete Users

- Admins can **update** student details such as name, batch, or course if corrections are needed.
- If necessary, **delete** a student’s record completely from the system.

> ✅ This functionality helps maintain an accurate and up-to-date student database.

4. **Mark Holidays**  

![Admin Mark Holidays](https://drive.google.com/uc?export=view&id=1qWbGwqaK7pW2p302jvdfzL6GnyjDPexv)

Admins can block specific days to prevent students from making reservations on those dates.  
This feature includes a set of controls for managing holiday entries efficiently.

#### 🧰 Interface Components:

- 📅 **Date Picker** – Select the date you want to mark as a holiday.
- 📝 **Reason TextBox** – Provide a reason or note for the holiday.
- 🔍 **Search Button** – Check if a holiday entry already exists for the selected date.
- 📋 **All Button** – View a list of all holidays and their reasons.
- 💾 **Save Button** – Save a new holiday date along with its reason.
- ✏️ **Edit Button** – Modify the reason for an already saved holiday.
- 🗑️ **Delete Button** – Completely remove a holiday entry.

#### ⚙️ Functional Behavior:

- When a date is selected via the **Date Picker** and a **reason** is entered, clicking **Save** will block that date from future reservations.
- Use **Edit** to update the reason for an existing holiday.
- **Delete** permanently removes the selected holiday date.
- **All** displays every date that has been marked as a holiday, along with reasons.
- Use **Search** after selecting a date to check whether it has already been saved as a holiday.

> ✅ This feature helps ensure that reservations are only possible on working days, maintaining proper scheduling discipline.


5. **Limit Weekly Reservations**  

![Admin Limit Weekly Reservations](https://drive.google.com/uc?export=view&id=1AcIAXb7IYwXsuR0_5thHmYilTg8mnAK8)

This feature allows the admin to control **how many reservations** a single student can make **within a week**.

A week is defined as starting from **Monday** and ending on **Sunday**.

#### ⚙️ Functionality:

- Admins can specify the **maximum number of reservations** allowed per student for each calendar week.
- Once the limit is reached, the student will be **restricted** from making additional reservations until the next week begins.
- This helps ensure **fair usage** of lab resources and gives all students equal opportunity.

> ✅ Especially useful in environments with limited PC availability and high student demand.


6. **Block Faulty PCs**  

![Admin Block Faulty PCs](https://drive.google.com/uc?export=view&id=1ipc7g5O-Z5qDzcuAFCKFb28GGZbIDwP9)

If a specific PC is malfunctioning or unavailable due to any issue, admins can use this feature to **block that PC** within the system.

#### ⚙️ Functionality:

- Blocked PCs will no longer appear in the reservation list for students.
- Students will be **unable to select or reserve** any PC that has been marked as faulty.
- This ensures a smooth user experience by preventing booking of unusable machines.

> ✅ Useful for maintaining reservation reliability and minimizing disruptions during practical sessions.

7. **Adjust Calendar Range**  

![Admin Adjust Calendar Range](https://drive.google.com/uc?export=view&id=1kPluyjJ6Azu7wnUQAhFbLNkzw-Bi-wE9)

This feature allows admins to define **how many days into the future** students are allowed to view and make reservations.

#### ⚙️ Functionality:

- The system starts counting from **today’s date**.
- Admins can configure the number of **future days** shown in the reservation calendar.
- Students will only be able to book sessions within this allowed date range.

> ✅ Helps control reservation visibility and limit far-ahead bookings.


8. **Block Specific Users**  

![Admin Block Specific Users](https://drive.google.com/uc?export=view&id=1pNd7To_t_SYkCCSi433zA-sg8e8skTH0)

Admins have the ability to **block individual students** from making reservations.

#### ⚙️ Functionality:

- A student can be blocked for disciplinary reasons or any other valid concern.
- Once blocked, the student will be **restricted from making any further reservations**.
- The block remains active until the admin manually unblocks the user.

> ✅ Useful for handling misuse of the system or enforcing specific policies.


9. **Export Backup Data**  

Admins can export all system data as a backup in either **Microsoft Excel** or **Microsoft Access** formats.

#### 📁 Features:

- Export includes: Registered users, reservations, holidays, blocked users, and system configurations.
- Useful for **data recovery**, **reporting**, or **migration** purposes.
- Backup files can be saved locally and reused later if needed.

> 🔐 Ensures data safety and gives flexibility for offline review or audits.


## 👤 User Features
