```mermaid
erDiagram
    %% Entities and attributes
    PRODUCTS {
        int product_id PK
        string model
        string brand
        float price
    }
    
    CUSTOMERS {
        int customer_id PK
        string first_name
        string last_name
        string email
        string phone
    }

    SALES {
        int sale_id PK
        int product_id FK
        int customer_id FK
        date sale_date
        int quantity
    }

    INVENTORY {
        int inventory_id PK
        int product_id FK
        int stock_level
    }

    %% Relationships with cardinalities
    PRODUCTS ||--o{ SALES : "1 to many"
    CUSTOMERS ||--o{ SALES : "1 to many"
    PRODUCTS ||--|{ INVENTORY : "1 to 1"
