# Medical Appointments Analysis
Analyze 100k medical appointments in Brazil focused on the question of what factors are important to predict if patients show up for their appointment.

## Project Overview
This project used a dataset with information from 100K medical appointments in Brazil that focused on whether the patient showed up for their appointment or were a no-show for their appointment. A number of characteristics about the patient are included in each row. Questions I focused on for this analysis:

- Which gender missed the highest percentage of appointments?
- Which days of the week have the highest percentage of missed appointments?
- Which age group has the highest percentage of missed appointments?

## Technology Used:
- Anaconda
- Jupyter Notebook
- Python
- Pandas
- Matplotlib
- Numpy
- Seaborn
- Github

#### Website:
[appointments.davidblackwelder.com](https://appointments.davidblackwelder.com)


### Gathering Data
The data was downloaded from Udacity and saved as `noshowappointments-kagglev2-may-2016.csv`.

### Assessing and Cleaning Data
A visual and programmatic assessment was performed within `Investigate_a_Dataset.ipynb`.

#### Quality and Tidiness Issues
- Converted `ScheduledDay` and `AppointmentDay` to datetime format.
- Create new columns for month, day, and year for both scheduled and appointment dates.
- Removed records where the appointment date was before the scheduled date.
- Removed columns not needed for this analysis (`Gender`, `PatientID`, `AppointmentID`, `Hipertension`, `Diabetes`, `Alcoholism`, `Handcap`).
- Renamed columns as needed.
- Dropped records where age was less than 0.
- Mapped ages to single integer

## Conclusions

### Insights
> _Analysis was done based on number of appointments and not by patients. Several of the records had to be removed due to data inaccuracies either in age or where the scheduled date was after the appointment day. The data is also limited in understanding why an appointment was missed. While the analysis can provide categorical insights, there were no inferential statistics performed during this analysis._

#### Appointments by Gender
<img src="./imgs/appt_made_vs_missed_by_gender.png">

From the analysis made we can see that females have the highest percentage of appointments and men show up to their appointments at a higher percentage of their appointments than women.

#### Appointments by Day
<img src="./imgs/appt_made_vs_missed_by_appt_day.png">

Tuesday and Wednesday account for 47.60% of all appointments. There are no appointments on Sunday. Thursday and Saturday have the highest percentage of appointments made. Monday and Wednesday have the highest percentage of appointments missed.

#### Appointments by Age Group
<img src="./imgs/appt_made_vs_missed_by_age_group.png">

Appointments for younger patients have a higher percentage of missed appointments than those of the older patients, excluding patients 100+ years old. Patients 100 years old or older miss 60% of their appointments.

## Extra
__Website:__ [appointments.davidblackwelder.com](https://appointments.com/davidblackwelder.com)
