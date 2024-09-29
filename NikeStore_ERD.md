```mermaid
```mermaid
erDiagram
    %% Entities and attributes
    PRODUCTS {
         product_id PK
         model
         brand
         price
    }
    
    CUSTOMERS {
        customer_id PK
        first_name
        last_name
        email
        phone
    }

    SALES {
         sale_id PK
         product_id FK
         customer_id FK
    }

    INVENTORY {
        inventory_id PK
        product_id FK
        stock_level
    }

    %% Relationships with cardinalities
    PRODUCTS ||--o{ SALES : "1 to many"
    CUSTOMERS ||--o{ SALES : "1 to many"
    PRODUCTS ||--|{ INVENTORY : "1 to 1"
```
