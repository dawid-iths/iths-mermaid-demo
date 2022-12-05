# iths-mermaid-demo

```mermaid
sequenceDiagram;
    Actor User;
    User->>+Bankomat: Put in Card;
    Bankomat-->>+User: Need Pin!;
    User->>+Bankomat: Set pincode!;
    Bankomat->>+BankSystem: Check pincode!;
    activate Bankomat;
    BankSystem-->>+Bankomat: Not a valid pin!;
    deactivate Bankomat;
    Bankomat-->>+User: Not a valid pin!;
    User->>+Bankomat: cancel!;
    Bankomat-->>+User: Card eject!;


