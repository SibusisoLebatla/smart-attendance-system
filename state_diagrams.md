```mermaid

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
