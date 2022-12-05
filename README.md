# iths-mermaid-demo

```mermaid
sequenceDiagram;
    Actor User;
    User->>+Bankomat: Put in Card;
    Bankomat-->>+User: Need Pin!;
    User->>+Bankomat: Set pincode!;
    Bankomat->>+BankSystem: Check pincode!;
    activate BankSystem;
    BankSystem-->>+Bankomat: Response!;
    deactivate BankSystem;
    Note over User,BankSystem: If not valid pin!;
    Bankomat-->>+User: Not a valid pin!;
    User->>+Bankomat: cancel!;
    Bankomat-->>+User: Card eject!;
    Note over User,BankSystem: If valid pin;


