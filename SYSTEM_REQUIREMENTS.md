# 🏫 Smart Attendance System - System Requirements Document (SRD)

## **📌 1. Functional Requirements**
The system shall:

1. **Allow students to check in using QR code or Face ID**  
   - ✅ *Acceptance Criteria:* QR scan should log attendance instantly.
2. **Enable teachers to generate attendance reports**  
   - ✅ *Acceptance Criteria:* Reports must be exportable in PDF/Excel.
3. **Authenticate users securely before granting access**  
   - ✅ *Acceptance Criteria:* Uses JWT for login sessions.
4. **Allow admin to add/edit/remove users**  
   - ✅ *Acceptance Criteria:* Admin can modify student/teacher details.
5. **Store attendance records in a database**  
   - ✅ *Acceptance Criteria:* Data must persist after logouts.
6. **Send real-time attendance notifications to parents**  
   - ✅ *Acceptance Criteria:* SMS should be received within 1 minute.
7. **Enable students to check past attendance logs**  
   - ✅ *Acceptance Criteria:* History available for up to 6 months.
8. **Support multiple campuses and class sections**  
   - ✅ *Acceptance Criteria:* Filters by campus, department, and section.
9. **Allow offline attendance logging (syncs later)**  
   - ✅ *Acceptance Criteria:* Data syncs automatically once online.
10. **Generate analytics on student attendance trends**  
   - ✅ *Acceptance Criteria:* Graphs and stats updated in real-time.

---

## **📌 2. Non-Functional Requirements**
| Category | Requirement |
|----------|------------|
| **Usability** | The interface shall comply with WCAG 2.1 accessibility standards. |
| **Deployability** | The system shall be deployable on Windows and Linux servers. |
| **Maintainability** | API documentation shall be provided for future integrations. |
| **Scalability** | The system must support **1,000 concurrent users** during peak hours. |
| **Security** | All user data shall be encrypted using **AES-256**. |
| **Performance** | Attendance check-in shall complete **within 2 seconds**. |
