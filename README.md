# iths-mermaid-demo

```mermaid
sequenceDiagram
    User->>+Bankomat: Put in Card
    Bankomat->>+User: Need Pin!
    User->>+Bankomat: Set pincode!
    Bankomat->>+BankSystem: Check pincode!

