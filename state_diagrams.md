```mermaid


stateDiagram-v2
    [*] --> Available
    Available --> Reserved : User reserves
    Reserved --> CheckedOut : User checks out
    CheckedOut --> Returned : User returns
    Returned --> Available : Library processes return
    CheckedOut --> Lost : Reported as lost
    Reserved --> Available : Reservation cancelled





stateDiagram-v2
    [*] --> Registered
    Registered --> Active : Email confirmed
    Active --> Suspended : Rule violation
    Suspended --> Active : Appeal granted
    Active --> Deleted : User deletes account




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



stateDiagram-v2
    [*] --> Initiated
    Initiated --> Verified : Validated
    Verified --> Successful : Paid
    Verified --> Failed : Insufficient funds



Notification
stateDiagram-v2
    [*] --> Queued
    Queued --> Sent : System triggers event
    Sent --> Read : User reads it




stateDiagram-v2
    [*] --> Assigned
    Assigned --> InProgress : Staff accepts
    InProgress --> Completed : Staff finishes
    Assigned --> Reassigned : Reallocation


Feedback
stateDiagram-v2
    [*] --> Submitted
    Submitted --> Reviewed : Admin reads feedback
    Reviewed --> Addressed : Action take


