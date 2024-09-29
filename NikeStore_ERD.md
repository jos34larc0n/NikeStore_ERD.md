```mermaid
erDiagram
    %% Entities and attributes
    PRODUCTS {
         product_id 
         model
         brand
         price
    }
    
    CUSTOMERS {
         customer_id 
         first_name
         last_name
         email
         phone
    }

    SALES {
         sale_id 
         product_id 
         customer_id 
    }

    INVENTORY {
        inventory_id 
        product_id 
        stock_level
    }

    %% Relationships with cardinalities
    PRODUCTS ||--o{ SALES : "1 to many"
    CUSTOMERS ||--o{ SALES : "1 to many"
    PRODUCTS ||--|{ INVENTORY : "1 to 1"
```
