
                         ┌──────────────────┐
                         │      ROLES       │
                         ├──────────────────┤
                         │ PK role_id       │
                         │ role_name        │
                         └────────┬─────────┘
                                  │
                                  │ 1
                                  │
                                  │ N
                         ┌────────▼─────────┐
                         │      USERS       │
                         ├──────────────────┤
                         │ PK user_id       │
                         │ role_id FK       │
                         │ name             │
                         │ email            │
                         │ password         │
                         │ phone            │
                         └──────┬─────┬─────┘
                                │     │
                     1          │     │ 1
                                │     │
                     N          │     │ N
                  ┌─────────────▼┐   ┌▼──────────────┐
                  │   ADDRESSES  │   │     CART      │
                  ├──────────────┤   ├───────────────┤
                  │ PK address_id│   │ PK cart_id    │
                  │ user_id FK   │   │ user_id FK    │
                  │ address      │   │ created_at    │
                  │ city         │   └───────┬───────┘
                  │ pincode      │           │
                  └──────────────┘           │ 1
                                             │
                                             │ N
                                    ┌────────▼────────┐
                                    │   CART_ITEMS    │
                                    ├─────────────────┤
                                    │ PK cart_item_id │
                                    │ cart_id FK      │
                                    │ product_id FK   │
                                    │ quantity        │
                                    └────────┬────────┘
                                             │ N
                                             │
                                             │ 1
                              ┌──────────────▼─────────────┐
                              │          PRODUCTS           │
                              ├─────────────────────────────┤
                              │ PK product_id               │
                              │ category_id FK              │
                              │ name                        │
                              │ description                 │
                              │ price                       │
                              │ stock_quantity              │
                              │ image                       │
                              │ status                      │
                              └──────────────┬──────────────┘
                                             │ N
                                             │
                                             │ 1
                                    ┌────────▼─────────┐
                                    │    CATEGORIES    │
                                    ├──────────────────┤
                                    │ PK category_id  │
                                    │ category_name   │
                                    │ description     │
                                    └──────────────────┘


                         ┌──────────────────┐
                         │      ORDERS      │
                         ├──────────────────┤
                         │ PK order_id      │
                         │ user_id FK       │
                         │ address_id FK    │
                         │ order_date       │
                         │ total_amount     │
                         │ order_status     │
                         └───────┬──────┬───┘
                                 │      │
                              1  │      │ 1
                                 │      │
                              N  │      │ 1
                    ┌────────────▼┐     ┌▼────────────────┐
                    │ ORDER_ITEMS │     │    PAYMENTS     │
                    ├─────────────┤     ├─────────────────┤
                    │ PK item_id  │     │ PK payment_id   │
                    │ order_id FK │     │ order_id FK     │
                    │ product_id FK│    │ payment_method  │
                    │ quantity    │     │ payment_status  │
                    │ price       │     │ payment_date    │
                    └──────┬──────┘     └─────────────────┘
                           │
                           │ N
                           │
                           │ 1
                           │
                     PRODUCTS


                         ┌──────────────────┐
                         │    DELIVERIES    │
                         ├──────────────────┤
                         │ PK delivery_id   │
                         │ order_id FK      │
                         │ delivery_user_id │
                         │ assigned_date    │
                         │ delivered_date   │
                         │ delivery_status  │
                         └────────┬─────────┘
                                  │
                                  │ N
                                  │
                                  │ 1
                                  ▼
                                USERS
                         (Delivery Staff)