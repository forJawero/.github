Welcome to Jawero, where innovation meets convenience in the world of shopping. At Jawero, we're redefining the shopping experience, empowering both buyers and sellers with a groundbreaking concept that transforms the way we buy and sell goods.

Our platform and tools turn any traditional physical shop of any size into a multivendor self-checkout shop. This removes from the seller the hassle of getting a physical store, reduces the time to market for the seller as well as eliminating several barriers to entry. With the self-checkout feature, the store can remain operational all night. Enhanced by our self-checkout feature, stores can now stay operational around the clock, ensuring uninterrupted convenience for all.

```mermaid
flowchart TB
classDef borderless stroke-width:0px
classDef darkBlue fill:#00008B, color:#fff
classDef brightBlue fill:#6082B6, color:#fff
classDef gray fill:#62524F, color:#fff
classDef gray2 fill:#4F625B, color:#fff
classDef red fill:#f00, color:#fff
classDef green fill:#111, color:#fff
classDef yellow fill:#fcba03, color:#fff
classDef azure fill:#F0FFFF, color:#000
classDef floralWhite fill:#FFFAF0, color:#000

subgraph vendors[Vendors]
    direction TB %%
    Vendor1[[Vendor 1 ]]
    Vendorn[[Vendor n ]]
    class Vendor1 brightBlue
    class Vendorn yellow
end
class vendors green

subgraph Jawero[Jawero]
    direction TB
    subgraph Inventory[ ]
        Inventory_[Inventory]
        class Inventory_ borderless
    end
    Inventory<-.->shops
    subgraph shops[Shops]
        direction TB
        subgraph shop_1[Shop 1]
            direction TB
            subgraph Seller1_1[Vendor 1]
                direction LR
                Item1_[Item 1]
                Item1_2[Item 2]
                Item1_n[Item n]
            end
            subgraph Sellern_1[Vendor n]
                Item2_[Item 1]
                Item2_2[Item 2]
                Item2_n[Item n]
            end
            class Seller1_1 brightBlue
            class Sellern_1 yellow
        end
        subgraph shop_n[Shop n]
            direction TB
            subgraph Seller1_2[Vendor 1]
                direction LR
                Item2_1_[Item 1]
                Item2_1_2[Item 2]
                Item2_1_n[Item n]
            end
            subgraph Sellern_2[Vendor n]
                Item2_2_[Item 1]
                Item2_2_2[Item 2]
                Item2_2_n[Item n]
            end
            class Seller1_2 brightBlue
            class Sellern_2 yellow
        end
    end
   
    subgraph Payment[ ]
        payment[Payment]
        class Inventory_ borderless
    end
    
    
    
end

subgraph Buyer[ ]
    buyer[[Shopper]]
end
class Buyer azure
subgraph Landlord[ ]
    landlord[[Landlord]]
end
class Landlord red

vendors--Supply-->shops
Buyer<--Searches-->Inventory
Inventory--Notifies-->vendors

Payment--Pays to-->vendors
Buyer--Pays to-->Payment
shops--picks from-->Buyer
Payment--Pays to-->Landlord
Landlord--Leases-->shops

```
