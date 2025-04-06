Book
stateDiagram-v2
    [*] --> Available
    Available --> Reserved : User reserves
    Reserved --> CheckedOut : User checks out
    CheckedOut --> Returned : User returns
    Returned --> Available : Library processes return
    CheckedOut --> Lost : Reported as lost
    Reserved --> Available : Reservation cancelled


Explanation:

Key States: Available, Reserved, CheckedOut, Returned, Lost

Transitions: Triggered by user actions such as reservation, checkout, and return.

Requirement Mapping:

FR-001: Book must be searchable and show availability.

FR-004: Allow checkout and return of books.

FR-005: Allow users to cancel reservations.


User Account
stateDiagram-v2
    [*] --> Registered
    Registered --> Active : Email confirmed
    Active --> Suspended : Rule violation
    Suspended --> Active : Appeal granted
    Active --> Deleted : User deletes account

Explanation:

Key States: Registered, Active, Suspended, Deleted

Requirement Mapping:

FR-002: User registration and login functionality.

FR-009: Allow users to delete accounts.

Order (Book Request)

stateDiagram-v2
    [*] --> Initiated
    Initiated --> Processing : Validated by system
    Processing --> Completed : Book dispatched
    Processing --> Canceled : User cancels or system fails

Explanation:

States: Initiated, Processing, Completed, Canceled

Requirement Mapping:

FR-007: Book request process

FR-005: Order cancelation

Payment 
stateDiagram-v2
    [*] --> Initiated
    Initiated --> Verified : Validated
    Verified --> Successful : Paid
    Verified --> Failed : Insufficient funds

Explanation:

Requirement Mapping:

FR-006: Secure online payment handling

Notification
stateDiagram-v2
    [*] --> Queued
    Queued --> Sent : System triggers event
    Sent --> Read : User reads it



stateDiagram-v2
    [*] --> Queued
    Queued --> Sent : System triggers event
    Sent --> Read : User reads it

Explanation:

Requirement Mapping:

FR-008: Notify users of actions like due dates and confirmations

Staff Task
stateDiagram-v2
    [*] --> Assigned
    Assigned --> InProgress : Staff accepts
    InProgress --> Completed : Staff finishes
    Assigned --> Reassigned : Reallocation

Feedback
stateDiagram-v2
    [*] --> Submitted
    Submitted --> Reviewed : Admin reads feedback
    Reviewed --> Addressed : Action taken
