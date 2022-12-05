# iths-mermaid-demo

```mermaid
sequenceDiagram;
    Actor User;
    User->>+Bankomat: Put in Card;
    Bankomat-->>+User: Need Pin!;
    User->>+Bankomat: Set pincode!;
    Bankomat->>+BankSystem: Verify pincode!;
    activate BankSystem;
    BankSystem-->>+Bankomat: Response!;
    deactivate BankSystem;
    Note over User,BankSystem: If not valid pin!;
    Bankomat-->>+User: Not a valid pin!;
    User->>+Bankomat: cancel!;
    Bankomat-->>+User: Card eject!;
    Note over User,BankSystem: If valid pin;
    User->>+Bankomat: Add sum!;
    Bankomat-->>+BankSystem: start transaction!;
    Note over Bankomat,BankSystem: Enough cash?;
    BankSystem-->>+Bankomat: yepp!;
    Bankomat-->>+User: Take my money $$$$!;
    Note over Bankomat,BankSystem: No money on account!;
    Bankomat-->>+User: Card eject!;
