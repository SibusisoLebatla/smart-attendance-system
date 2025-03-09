# 🎭 Smart Attendance System - Reflection on Stakeholder Challenges

## **📌 Challenges in Balancing Stakeholder Needs**
During the requirement engineering process, we encountered several challenges in addressing different stakeholder needs.

### **1️⃣ Conflict Between Security and Ease of Access**
- Students wanted **quick and easy access** (single-step login).  
- IT Staff required **strong security** (multi-factor authentication).  
- **Solution:** Implement **secure QR login**, reducing the need for passwords while maintaining security.

### **2️⃣ Performance vs. Scalability**
- IT Staff required the system to handle **large numbers of students concurrently**.  
- Administrators wanted **real-time analytics**, which increased **server load**.  
- **Solution:** Optimized **database indexing** and implemented **load balancing**.

### **3️⃣ User Experience Challenges**
- Teachers wanted a **detailed but easy-to-use** report dashboard.  
- **Solution:** Designed a **simplified UI with export options**.

### **4️⃣ Deployment and Maintenance Trade-offs**
- IT Staff required **regular updates** but didn't want frequent downtime.  
- **Solution:** Introduced **rolling updates** with **zero downtime deployments**.

---
## **📌 Lessons Learned**
Balancing stakeholder needs requires **compromise and prioritization**. By carefully analyzing trade-offs and implementing **flexible, scalable solutions**, we ensured that all users had a **satisfying experience** without compromising **performance, security, or usability**.
