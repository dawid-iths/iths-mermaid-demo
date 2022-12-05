# iths-mermaid-demo

```mermaid
sequenceDiagram;
    Alice->>+John: Hello John, how are you?
    Alice->>+John: John, can you hear me?
    John-->>-Alice: Hi Alice, I can hear you!
    John-->>-Alice: I feel great!
    Actor User;
        User->>+Bankomat: Put in Card;
        
        Bankomat-->>+User: Type in your Pincode!;
        User->>+Bankomat: Set pincode!;
    
    Bankomat->>+BankSystem: Verify pincode!;
    
    activate BankSystem;
        BankSystem-->>+Bankomat: Response true / false!;
    deactivate BankSystem;
    
    alt false;
        Bankomat-->>+User: Not a valid pin!;
        User->>+Bankomat: press cancel button;
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
    
