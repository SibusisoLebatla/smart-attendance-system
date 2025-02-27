# 🏫 Smart Attendance System - Architecture  

## 1️⃣ System Overview  
The **Smart Attendance System** is designed to automate student attendance tracking using **QR codes** and **Facial Recognition**.  
It ensures **real-time attendance monitoring**, reduces fraud, and provides comprehensive attendance reports.  

### **📌 Technology Stack**  
- **Frontend:** React.js (for a dynamic web interface)  
- **Backend:** Node.js & Express.js (for API handling)  
- **Database:** MySQL (to store attendance records)  
- **Authentication:** JWT (for secure login)  
- **Hosting:** Vercel (Frontend), AWS (Backend)  

---

## **2️⃣ System Diagrams**  

### **🌐 Context Diagram**  
Shows how different users interact with the system.  

```mermaid
graph TD;
  A[Student] -->|Scans QR Code / Face ID| B(Smart Attendance System);
  C[Teacher] -->|Views Attendance Logs| B;
  D[Admin] -->|Manages Student Records| B;
graph TD;
  A[Student] -->|Uses Web App| B[Frontend (React)];
  B -->|Sends API Requests| C[Backend (Node.js)];
  C -->|Stores & Retrieves Data| D[MySQL Database];
  E[Teacher] -->|Views Reports| B;
  F[Admin] -->|Manages Students| B;
graph TD;
  A[API Controller] -->|Handles HTTP Requests| B[Auth Service];
  A -->|Processes Attendance Data| C[Attendance Service];
  C -->|Stores Data| D[Database Connector];
  B -->|Validates Users| D;
