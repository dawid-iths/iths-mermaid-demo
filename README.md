# iths-mermaid-demo

```mermaid
sequenceDiagram;
    Actor User;
    
    User->>+Bankomat: Put in Card;
    Bankomat-->>-User: Type in your Pincode!;
    User->>+Bankomat: Set pincode!;
    activate Bankomat;
        Bankomat->>+BankSystem: Verify pincode!;

        BankSystem-->>-Bankomat: Response true / false!;

        alt false;
            Bankomat-->>+User: Not a valid pin!;
            User->>+Bankomat: press cancel button;
            Bankomat-->>+User: Card eject!;
        end;
        alt true;
        Bankomat-->>-User: valid pin!;
    deactivate Bankomat;
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
    
