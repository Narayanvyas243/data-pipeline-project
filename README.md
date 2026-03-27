#  AWS Data Pipeline: RDS to S3 using DMS

##  Overview

This project demonstrates a cloud-based data pipeline built on AWS, where data is extracted from a MySQL database hosted on Amazon RDS and migrated to Amazon S3 using AWS Database Migration Service (DMS).

The pipeline simulates a real-world ETL (Extract, Transform, Load) workflow, enabling scalable and cost-efficient data movement for analytics and storage.

---

##  Architecture

RDS (MySQL) → AWS DMS → Amazon S3

* **Amazon RDS (MySQL)**: Source database containing structured data (`college_db` with `student_attendance` table).
* **AWS DMS**: Handles data migration from RDS to S3.
* **Amazon S3**: Stores exported data as CSV files (data lake layer).

---

##  Technologies Used

* AWS RDS (MySQL 8.0)
* AWS DMS (Database Migration Service)
* Amazon S3
* IAM Roles & Security Groups
* MySQL (for data creation and queries)

---

##  Dataset

The dataset contains student attendance records with attributes like:

* Student ID
* Full Name (unique Indian names)
* Course
* Attendance Percentage
* Contact Number
* City
* Timestamp

---

##  Workflow

1. Created a MySQL database (`college_db`) in AWS RDS.
2. Designed and populated the `student_attendance` table.
3. Configured AWS DMS replication instance (free-tier eligible).
4. Created source endpoint (RDS) and target endpoint (S3).
5. Configured migration task to transfer data.
6. Data successfully exported to S3 bucket (`raw-data-bucket-narayan`).

---

##  Key Features

* Fully cloud-based pipeline
* Free-tier optimized (no cost architecture)
* Secure connection using IAM and Security Groups
* Real-time scalable architecture (can be extended)

---

##  Output

The data is stored in Amazon S3 in CSV format, ready for analytics tools like Athena, Power BI, or further processing.

---

##  Demo Video

A complete walkthrough of the project is available in this repository (uploaded using Git LFS).

---

##  Future Enhancements

* Add AWS Glue for transformation
* Query data using Amazon Athena
* Build dashboards using QuickSight / Power BI
* Automate pipeline using EventBridge

---
##  How to Access Demo Video

This repository uses Git LFS to store large files (like the demo video).

### Steps to access the video:

1. Install Git LFS:

   ```bash
   git lfs install
   ```

2. Clone the repository:

   ```bash
   git clone <your-repo-url>
   ```

3. Pull LFS files:

   ```bash
   git lfs pull
   ```

4. Navigate to the video file and open it locally.

---

 Note: If the video does not load on GitHub preview, download it after running `git lfs pull`.
