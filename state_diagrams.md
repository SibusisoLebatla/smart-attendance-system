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



