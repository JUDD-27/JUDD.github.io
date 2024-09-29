# NikeStore_ERD.md
```mermaid
erDiagram 
    Product {
        String ProductID PK
        String Name
        Decimal price
        int stock
    }

    Customer {
        String custumerID PK
        String name
        string Email

    }

    Sale {
        String saleID PK
        String product FK
        String customerID FK
        date saleDate
        int quantity
    }
     
     Inventory {
        string producID PK
        int unit

     }


Product ||--o{ Sale : "sold in"
Customer ||--o{ Sale : "buys"
Product ||--o{ Inventory : "has"

```

# Store Diagraman

  **Product** | **Customer** | **Sale** | **Inventory**    
  ----------- | ------------ | -------- | ---------------
  shoes offered in store | personal information | products tagged under sales | quantity of availiabilty 

