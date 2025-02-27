Title :The Architecture Side of the Snart Attendance System

Overview:

The system allows both students and lectures to mark their presence using QR code or facial recognision while providing real-time tracking that can be viewed by students, lectures as well as the administrations.

Technology behind:

** Frontend:** HTML, CSS, JavaScript(React and React Native)
**Backend:** Node.js 
**Database:** MySQL
**Authentication:** JWT for secure login
**Hosting:** Github and Vercel for frontend , AWS fro backend

## C4 Diagrams

 Showing the different usage of the system from the perspective of Students, Lectures and Administrators.

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

