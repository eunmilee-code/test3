# test3
```mermaid



    sequenceDiagram
    participant Customer as Customer
    participant ReservationSystem as Reservation System
    participant Room as Room
    participant PaymentSystem as Payment System
    
    Customer->>ReservationSystem: RequestRoomReservation()
    ReservationSystem->>Room: CheckAvailability()
    Room-->>ReservationSystem: AvailabilityStatus()
    ReservationSystem->>Customer: DisplayRoomOptions()
    Customer->>ReservationSystem: SelectRoom()
    ReservationSystem->>PaymentSystem: RequestPayment()
    PaymentSystem-->>Customer: RequestPaymentDetails()
    Customer->>PaymentSystem: ProvidePaymentDetails()
    PaymentSystem->>ReservationSystem: ConfirmPayment()
    ReservationSystem->>Room: ReserveRoom()
    Room-->>ReservationSystem: ConfirmReservation()
    ReservationSystem->>Customer: ProvideReservationConfirmation()

