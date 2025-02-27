# Smart Attendance System - Architecture  

## 1. System Overview  
The **Smart Attendance System** allows students to mark attendance using facial recognition or QR codes while providing real-time tracking for teachers and administrators.  

### **Technology Stack**  
- **Frontend:** HTML, CSS, JavaScript (React)  
- **Backend:** Node.js (Express.js)  
- **Database:** MySQL  
- **Authentication:** JWT for secure login  
- **Hosting:** GitHub & Vercel for frontend, AWS for backend  

---

## 2. C4 Diagrams  

### **2.1 Context Diagram**  
The **Context Diagram** shows how different users interact with the system.  

```mermaid
C4Context
  title Smart Attendance System - Context Diagram
  Enterprise_Boundary(b0, "School Network") {
    System(s1, "Smart Attendance System", "Manages student attendance")
    Person(p1, "Student", "Uses QR Code or Face ID for attendance")
    Person(p2, "Teacher", "Views attendance reports")
    Person(p3, "Admin", "Manages students & generates reports")

    p1 -> s1 : "Scans QR Code / Face ID"
    p2 -> s1 : "Checks attendance logs"
    p3 -> s1 : "Manages student records"
  }
C4Container
  title Smart Attendance System - Container Diagram
  System_Boundary(sas, "Smart Attendance System") {
    Container(c1, "Frontend (React)", "User Interface")
    Container(c2, "Backend (Node.js)", "Handles authentication & attendance processing")
    ContainerDb(db, "MySQL Database", "Stores student & attendance records")

    Person(p1, "Student", "Scans QR Code / Face ID")
    Person(p2, "Teacher", "Views attendance logs")

    p1 -> c1 : "Access via web browser"
    p2 -> c1 : "Access reports"
    c1 -> c2 : "API Requests (Login, Mark Attendance, View Records)"
    c2 -> db : "Stores/Retrieves Data"
  }
C4Component
  title Smart Attendance System - Component Diagram
  Container_Boundary(c2, "Backend (Node.js)") {
    Component(api, "API Controller", "Handles HTTP Requests")
    Component(auth, "Auth Service", "JWT Authentication")
    Component(attendance, "Attendance Service", "Processes attendance data")
    Component(db, "Database Connector", "Handles MySQL queries")

    api -> auth : "Validates User"
    api -> attendance : "Processes QR Code / Face Data"
    attendance -> db : "Stores Attendance Records"
  }
