# User Story Template

**Title:**
_As a [user role], I want [feature/goal], so that [reason]._

**Acceptance Criteria:**
1. [Criteria 1]
2. [Criteria 2]
3. [Criteria 3]

**Priority:** [High/Medium/Low]
**Story Points:** [Estimated Effort in Points]
**Notes:**
- [Additional information or edge cases]






# Admin User Stories

## User Story 1 — Admin Login
**Title:**  
_As an Admin, I want to log into the portal with my username and password, so that I can manage the platform securely._

**Acceptance Criteria:**  
1. The admin can access a login page with username and password fields.  
2. The system validates credentials against the database.  
3. Upon successful login, the admin is redirected to the dashboard.  

**Priority:** High  
**Story Points:** 3  
**Notes:**  
- Ensure password hashing for security.  

---

## User Story 2 — Admin Logout
**Title:**  
_As an Admin, I want to log out of the portal, so that I can protect system access when I finish my tasks._

**Acceptance Criteria:**  
1. The admin can log out from any page using a visible logout button.  
2. The session ends immediately upon logout.  
3. The system redirects the admin to the login page after logout.  

**Priority:** Medium  
**Story Points:** 2  
**Notes:**  
- Ensure session tokens are invalidated.  

---

## User Story 3 — Add Doctor
**Title:**  
_As an Admin, I want to add doctors to the portal, so that they can access the system and manage appointments._

**Acceptance Criteria:**  
1. The admin can input doctor details (name, specialization, contact info).  
2. The system validates all mandatory fields before saving.  
3. A success message appears after adding the doctor.  

**Priority:** High  
**Story Points:** 5  
**Notes:**  
- Data should save to the doctors table.  

---

## User Story 4 — Delete Doctor Profile
**Title:**  
_As an Admin, I want to delete a doctor’s profile from the portal, so that I can remove inactive or duplicate accounts._

**Acceptance Criteria:**  
1. The admin can select a doctor to delete.  
2. The system asks for confirmation before deletion.  
3. Once confirmed, the doctor’s record is removed from the database.  

**Priority:** Medium  
**Story Points:** 3  
**Notes:**  
- Include a confirmation popup to avoid accidental deletion.  

---

## User Story 5 — Run Stored Procedure
**Title:**  
_As an Admin, I want to run a stored procedure in MySQL CLI to get the number of appointments per month, so that I can track usage statistics._

**Acceptance Criteria:**  
1. The stored procedure returns total appointments grouped by month.  
2. The output displays month names and counts.  
3. The procedure runs without errors.  

**Priority:** High  
**Story Points:** 4  
**Notes:**  
- Example: `CALL GetMonthlyAppointments();`
