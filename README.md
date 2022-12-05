# iths-mermaid-demo

```mermaid
sequenceDiagram
    Actor User
    User->>+Bankomat: Put in Card
    Bankomat-->>+User: Need Pin!
    User->>+Bankomat: Set pincode!
    Bankomat->>+BankSystem: Check pincode!
    BankSystem-->>+Bankomat: Not a valid pin!
    Bankomat-->>+User: Not a valid pin!
    User->>+Bankomat: cancel!
    Bankomat-->>+User: Card eject!;
    
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;

