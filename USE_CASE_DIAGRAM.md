```mermaid
graph TD;
  A[Student] -->|Logs In| B[System]
  A -->|Registers for Attendance| C[Register Attendance]
  A -->|Views Attendance History| D[View Attendance]
  B -->|Manages Attendance Records| E[Admin]
  E -->|Generates Reports| F[Generate Report]
  A -->|Requests Support| G[Help Desk]
  E -->|Adds New Users| H[Manage Users]
  A -->|Receives Notifications| I[Notification System]
  A -->|Logs Out| J[System Logout]
