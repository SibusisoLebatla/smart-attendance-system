```mermaid

flowchart TD
    A[Start] --> B[Fill Registration Form]
    B --> C[Validate Inputs]
    C --> D{Valid?}
    D -- Yes --> E[Create Account]
    D -- No --> F[Show Error]
    E --> G[Send Confirmation Email]
    G --> H[End]

flowchart TD
    A[Start] --> B[Search for Book]
    B --> C[View Details]
    C --> D[Check Availability]
    D --> E{Available?}
    E -- Yes --> F[Checkout Book]
    E -- No --> G[Show Message]
    F --> H[Update Inventory]
    H --> I[Send Confirmation]
    I --> J[End]
