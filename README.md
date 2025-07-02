# **Medical Appointment No-Show Analysis**

## **Project Overview**

This project investigates factors influencing whether patients show up for their medical appointments in Brazil. The dataset contains over **110,000 medical appointments** with patient demographics, appointment details, and health conditions. The goal is to understand what affects appointment attendance, which can help healthcare providers improve scheduling and reduce missed appointments.

*Dataset source:* [Kaggle - No Show Appointments](https://www.kaggle.com/datasets/joniarroba/noshowappointments)

---

## **Dataset Description**

The dataset includes **14 columns**:

- **PatientId**: Unique identifier for each patient  
- **AppointmentID**: Unique identifier for each appointment  
- **Gender**: Male or Female  
- **ScheduledDay**: When the appointment was scheduled  
- **AppointmentDay**: When the appointment is to take place  
- **Age**: Patient’s age in years  
- **Neighbourhood**: Location of the patient  
- **Scholarship**: Enrolled in welfare program (**1 = Yes, 0 = No**)  
- **Hipertension**: Has high blood pressure (**1 = Yes, 0 = No**)  
- **Diabetes**: Has diabetes (**1 = Yes, 0 = No**)  
- **Alcoholism**: History of alcoholism (**1 = Yes, 0 = No**)  
- **Handcap**: Disability status (**0 = none, 1+ = various levels**)  
- **SMS_received**: Received SMS reminder (**1 = Yes, 0 = No**)  
- **No-show**: Whether patient missed appointment (**“Yes” = no show, “No” = showed up**)

---

## **Research Questions**

- **Does a patient’s age affect their likelihood of missing an appointment?**  
- **Does receiving an SMS reminder reduce no-show rates?**  
- **Does receiving a welfare scholarship affect attendance?**

---

## **Data Wrangling and Cleaning**

- Converted **“No-show”** column to binary values (**Yes = 1, No = 0**)  
- Converted date columns to **datetime** format  
- Removed invalid rows with **negative ages**  
- Consolidated handicap levels (**2, 3, 4 replaced with 1**) for consistency  
- Checked for **duplicates** and **missing values**

---

## **Exploratory Data Analysis**

- **Age:** No-show rates tend to increase slightly with very old age (>100 years).  
- **SMS Reminders:** Patients who received SMS reminders still showed a **28% no-show rate**, but this was lower than those who didn’t receive reminders.  
- **Scholarship:** Patients with welfare scholarships had a slightly different no-show rate, suggesting socioeconomic factors may play a role.  
- **Health Conditions:** Examined how hypertension, diabetes, alcoholism, and handicap status relate to attendance; results showed minor variations.

Visualizations include **histograms, boxplots,** and **bar charts** illustrating these relationships.

---

## **Conclusions**

- SMS reminders and patient age have some association with appointment attendance.  
- Patients with welfare scholarships or certain health conditions show minor variations in no-show rates.  
- No statistical tests were performed, so causation cannot be established, only observed trends.



