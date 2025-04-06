```mermaid

flowchart TD
    A[Start] --> B[Fill Registration Form]
    B --> C[Validate Inputs]
    C --> D{Valid?}
    D -- Yes --> E[Create Account]
    D -- No --> F[Show Error]
    E --> G[Send Confirmation Email]
    G --> H[End]
