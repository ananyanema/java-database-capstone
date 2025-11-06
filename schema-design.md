## MySQL Database Design

### Table: patients
- id: INT, Primary Key, Auto Increment
- name: VARCHAR(100), Not Null
- email: VARCHAR(100), Unique, Not Null
- phone: VARCHAR(15), Not Null
- date_of_birth: DATE
- created_at: DATETIME, Not Null
- updated_at: DATETIME

### Table: doctors
- id: INT, Primary Key, Auto Increment
- name: VARCHAR(100), Not Null
- specialization: VARCHAR(50)
- email: VARCHAR(100), Unique
- phone: VARCHAR(15)
- created_at: DATETIME, Not Null
- updated_at: DATETIME

### Table: appointments
- id: INT, Primary Key, Auto Increment
- doctor_id: INT, Foreign Key → doctors(id)
- patient_id: INT, Foreign Key → patients(id)
- appointment_time: DATETIME, Not Null
- duration: INT (minutes)
- status: INT (0=Scheduled, 1=Completed, 2=Cancelled)
- created_at: DATETIME, Not Null
- updated_at: DATETIME

### Table: admin
- id: INT, Primary Key, Auto Increment
- username: VARCHAR(50), Unique, Not Null
- password: VARCHAR(255), Not Null
- created_at: DATETIME, Not Null
- updated_at: DATETIME

### Optional Tables

#### Table: clinic_locations
- id: INT, Primary Key, Auto Increment
- name: VARCHAR(100), Not Null
- address: VARCHAR(255)
- phone: VARCHAR(15)

#### Table: payments
- id: INT, Primary Key, Auto Increment
- appointment_id: INT, Foreign Key → appointments(id)
- amount: DECIMAL(10,2), Not Null
- payment_method: VARCHAR(50)
- status: INT (0=Pending, 1=Paid)
- created_at: DATETIME, Not Null

---

## MongoDB Collection Design

### Collection: prescriptions
```json
{
  "_id": "ObjectId('64abc123456')",
  "patientId": 1,
  "appointmentId": 51,
  "medication": "Paracetamol",
  "dosage": "500mg",
  "doctorNotes": "Take 1 tablet every 6 hours.",
  "refillCount": 2,
  "pharmacy": {
    "name": "Walgreens SF",
    "location": "Market Street"
  },
  "tags": ["pain", "fever"],
  "createdAt": "2025-11-06T10:00:00Z",
  "updatedAt": "2025-11-06T10:00:00Z"
}

