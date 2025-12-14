# Use Case: Cloud-Based Chemo Scheduling & Chair Utilization Support

## Problem Statement

Oncology infusion centers face ongoing challenges with chemotherapy scheduling due to limited nursing availability, fluctuating daily capacity, and inaccurate estimates of chemotherapy chair time. In our current setting, schedulers are responsible for coordinating appointments for approximately 90 active chemotherapy patients. Because nurse staffing is limited, some patients remain unscheduled until the day before their intended treatment, relying on last-minute cancellations to secure an appointment.

An additional challenge is that **scheduled chair times often do not accurately reflect actual infusion duration**. Variability in regimen complexity, preparation delays, and patient-specific factors can cause treatments to run shorter or longer than planned. This leads to inefficient use of infusion chairs, overbooked days, and underutilized capacity on others.

This project proposes a **cloud-based chemo scheduling and chair utilization support system** designed to improve visibility into scheduling capacity and chair-time accuracy. The system supports operational decision-making for **schedulers, nurse managers, and clinic administrators** by providing summary analytics and capacity insights. All data used is **synthetic or de-identified** and intended strictly for educational purposes.

## Users

* **Schedulers**: Upload scheduling data and identify days with capacity risk.
* **Nurse Managers**: Review staffing capacity and chair utilization trends.
* **Clinic Administrators**: Monitor operational efficiency and planning metrics.

## Data Sources

The system uses simple, structured datasets commonly found in oncology operations:

* **Scheduled appointments (CSV)**

  * Appointment date
  * Regimen category (short / medium / long)
  * Scheduled chair minutes
  * Appointment status (scheduled, cancelled, completed)

* **Actual chair time (CSV)**

  * Appointment ID
  * Actual start and end times
  * Total chair minutes used

* **Nurse capacity data (CSV)**

  * Date
  * Number of nurses available
  * Maximum chairs supported

All patient identifiers are fictitious and no protected health information (PHI) is included.

## Basic Workflow

1. A scheduler uploads updated scheduling, chair-time, and nurse capacity CSV files through a simple web interface or API.
2. Raw files are stored securely in cloud object storage.
3. A serverless function or containerized job processes the data, validating formats and calculating scheduled versus actual chair-time differences.
4. Cleaned and aggregated data is loaded into a managed SQL database.
5. A cloud-based analytics notebook calculates utilization metrics and identifies days at risk due to staffing or chair-time inaccuracies.
6. A lightweight dashboard or API displays summary statistics, including capacity gaps, utilization percentages, and trends over time.

This workflow demonstrates how cloud storage, compute, databases, and analytics services can be integrated to address a realistic healthcare operations problem in oncology.

