#The Architecture Side of the Snart Attendance System

#Overview 
The system allows both students and lectures to mark their presence using QR code or facial recognision while providing real-time tracking that can be viewed by students, lectures as well as the administrations.

##Technology behind
** Frontend:** HTML, CSS, JavaScript(React and React Native)
**Backend:** Node.js 
**Database:** MySQL
**Authentication:** JWT for secure login
**Hosting:** Github and Vercel for frontend , AWS fro backend

## C4 Diagrams

 Showing the different usage of the system from the perspective of Students, Lectures and Administrators.

C4Context
   *title:* Smart Attendance System
   Enterprise_Boundary(b0, "School Network")
   {
   System(s1, "Smart Attendance System", "Manages student attendance")
   Person(p1, "Student", "User QR code or Face ID for attendance")
   Person(p2, "Teacher", "Views attendance reports")
   Person(p3, "Admin", "Manages students & geerates reports attendance percentages")

p1 -> s1 : "Scans QR Code / Face ID"
p2 -> s1 : "Checks attendance logs"
p3 -> s1 : "Manages student records"
}
