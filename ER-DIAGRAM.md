# Data Model (ER Diagram) - Hotel Booking System

\`\`\`mermaid
erDiagram
    CUSTOMER ||--o{ BOOKING : makes
    BOOKING ||--|| ROOM : reserves
    BOOKING ||--o{ PACKAGE : includes
    BOOKING ||--|| PAYMENT : has
    BOOKING ||--o| CANCELLATION : may_have
    ROOM ||--o{ ROOMTYPE : belongs_to
    MANAGER ||--o{ ROOM : manages
    RECEPTIONIST ||--o{ BOOKING : checks_in_out

    CUSTOMER {
        int customer_id
        string name
        string email
        string phone
    }
    ROOM {
        int room_id
        string room_type
        decimal price
        int capacity
        string status
    }
    BOOKING {
        int booking_id
        int customer_id
        int room_id
        date checkin_date
        date checkout_date
        int guest_count
        string status
    }
    PAYMENT {
        int payment_id
        int booking_id
        string method
        decimal amount
        string status
    }
    CANCELLATION {
        int cancel_id
        int booking_id
        date cancel_date
        decimal fee
    }
    PACKAGE {
        int package_id
        string name
        decimal price
    }
\`\`\`
