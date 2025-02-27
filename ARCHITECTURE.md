# 🏫 Smart Attendance System - Architecture  

## 1️⃣ System Overview  
The **Smart Attendance System** automates student attendance tracking using **QR codes** and **Facial Recognition**.  
It ensures **real-time attendance monitoring**, reduces fraud, and provides comprehensive attendance reports.  

### **📌 Technology Stack**  
- **Frontend:** React.js (for a dynamic web interface)  
- **Backend:** Node.js & Express.js (for API handling)  
- **Database:** MySQL (to store attendance records)  
- **Authentication:** JWT (for secure login)  
- **Hosting:** Vercel (Frontend), AWS (Backend)  

---

## **2️⃣ System Architecture Diagram**  

```mermaid
graph TD
  %% Context Diagram
  A[Student] -->|Scans QR Code / Face ID| B(Smart Attendance System)
  C[Teacher] -->|Views Attendance Logs| B
  D[Admin] -->|Manages Student Records| B

  %% Container Diagram
  subgraph System Components
    B1[Frontend (React)] -->|Sends API Requests| B2[Backend (Node.js)]
    B2 -->|Stores & Retrieves Data| B3[MySQL Database]
    E[Teacher] -->|Views Reports| B1
    F[Admin] -->|Manages Students| B1
  end

  %% Component Diagram
  subgraph Backend Services
    C1[API Controller] -->|Handles HTTP Requests| C2[Auth Service]
    C1 -->|Processes Attendance Data| C3[Attendance Service]
    C3 -->|Stores Data| C4[Database Connector]
    C2 -->|Validates Users| C4
  end
