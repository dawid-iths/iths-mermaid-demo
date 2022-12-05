# iths-mermaid-demo

```mermaid
sequenceDiagram
    User->>+Bankomat: Put in Card
    Bankomat->>+User: Need Pin!
    User->>+Bankomat: Set pincode!
    Bankomat->>+BankSystem: Check pincode!
    BankSystem->>+Bankomat: Not a valid pin!
    Bankomat->>+User: Not a valid pin!
    User->>+Bankomat: cancel!
    Bankomat->>+User: Card eject!

