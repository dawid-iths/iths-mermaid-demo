# iths-mermaid-demo

```mermaid
sequenceDiagram;
    Actor User;
    User->>+Bankomat: Put in Card;
    Bankomat-->>+User: Need Pin!;
    User->>+Bankomat: Set pincode!;
    Bankomat->>+BankSystem: Verify pincode!;
    activate BankSystem;
        BankSystem-->>+Bankomat: Response true / false!;
    deactivate BankSystem;
    alt false;
        Note over User,BankSystem: If not valid pin!;
        Bankomat-->>+User: Not a valid pin!;
        User->>+Bankomat: cancel!;
        Bankomat-->>+User: Card eject!;
    end;
    alt true;
        User->>+Bankomat: Add sum!;
    end;
        activate BankSystem;
        Bankomat-->>+BankSystem: start transaction!;
        Note over Bankomat,BankSystem: Enough cash?;
        BankSystem-->>+Bankomat: yepp!;
        Bankomat-->>+User: Take my money $$$$!;
    Note over Bankomat,BankSystem: No money on account!;
    BankSystem-->>+User: no money!;
    deactivate BankSystem;
    Bankomat-->>+User: Card eject!;
  
