## Use Case: Cloud-Based Chemo Scheduling & Chair Utilization Support

### <ins>Problem</ins>

Oncology infusion centers face ongoing challenges with chemotherapy scheduling due to limited nursing availability, fluctuating daily capacity, and inaccurate chair time estimates. Schedulers coordinate appointments for over 90 active chemotherapy patients. Because of limited nurse staffing, some patients remain unscheduled until the day before treatment and depend on last-minute cancellations to get an appointment.

Scheduled chair times often do not reflect actual infusion duration. Variability in regimen complexity, preparation delays, and patient needs can make treatments run shorter or longer than planned. This causes inefficient use of infusion chairs, overbooked days, and underutilized capacity on other days.

This project introduces a cloud-based system to help with chemo scheduling and chair use. It aims to give schedulers, nurse managers, and clinic administrators a clearer view of capacity and more accurate chair-time estimates by providing summary analytics and capacity insights. This project does not contain any real personal information and is used only for educational purposes.

### <ins>Users</ins>

* **Schedulers:** Upload scheduling data and identify days with capacity risk.
* **Nurse Managers:** Review staffing capacity and chair utilization trends.
* **Clinic Administrators:** Monitor operational efficiency and planning metrics.

### <ins>Data Sources</ins>

The system uses simple, structured datasets commonly found in oncology operations:

* **Scheduled appointments (CSV)**
  * Appointment date
  * Regimen category (short / medium / long)
  * Scheduled chair minutes
  * Appointment status (scheduled, cancelled, completed)
* **Actual chair time (CSV)**
  * Encounter ID
  * Actual start and end times
  * Total chair minutes used
* **Nurse capacity data (CSV)**
  * Date
  * Number of nurses available
  * Maximum chairs supported

> [!NOTE]
> **All patient identifiers are fictitious and no protected health information (PHI) is included.**

### <ins>Basic Workflow</ins>

1. A scheduler uploads updated scheduling, chair-time, and nurse capacity CSV files through a simple web interface or API.
2. Raw files are stored securely in cloud object storage.
3. A serverless function or containerized job processes the data, checks the formats, and calculates the differences between scheduled and actual chair times.
4. Cleaned and aggregated data is loaded into a managed SQL database.
5. A cloud-based analytics notebook calculates how well chairs are used and identifies days that may be at risk due to staffing or chair-time errors.
6. A simple dashboard or API displays summary statistics, such as capacity gaps, utilization percentages, and trends over time.

> [!IMPORTANT]
> **This workflow demonstrates how to integrate cloud storage, compute, databases, and analytics services to address a realistic healthcare operations problem in oncology.**

