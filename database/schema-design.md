# MySQL Schema Design – Clinic Management System

## Tables

### 1. Admin
| Field | Type | Description |
|-------|------|-------------|
| id | INT | Primary Key |
| username | VARCHAR(50) | Admin username |
| password | VARCHAR(100) | Encrypted password |

### 2. Doctor
| Field | Type | Description |
|-------|------|-------------|
| id | INT | Primary Key |
| name | VARCHAR(100) | Doctor's name |
| specialization | VARCHAR(100) | Field of expertise |
| email | VARCHAR(100) | Contact email |
| phone | VARCHAR(15) | Contact number |
| years_of_experience | INT | Years of experience |

### 3. Patient
| Field | Type | Description |
|-------|------|-------------|
| id | INT | Primary Key |
| name | VARCHAR(100) | Full name |
| email | VARCHAR(100) | Email address |
| phone | VARCHAR(15) | Contact number |
| address | VARCHAR(255) | Residential address |

### 4. Appointment
| Field | Type | Description |
|-------|------|-------------|
| id | INT | Primary Key |
| doctor_id | INT | Foreign Key (Doctor) |
| patient_id | INT | Foreign Key (Patient) |
| appointment_date | DATE | Date of appointment |
| appointment_time | TIME | Time slot |
| status | VARCHAR(50) | Scheduled / Completed / Cancelled |

### 5. Doctor Available Times
| Field | Type | Description |
|-------|------|-------------|
| id | INT | Primary Key |
| doctor_id | INT | Foreign Key (Doctor) |
| day_of_week | VARCHAR(20) | Availability day |
| start_time | TIME | Start time |
| end_time | TIME | End time |
