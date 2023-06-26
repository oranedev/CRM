# CRM
CRM flowchart using Python code
# Example ERD for a store database
# Entities
class Customer:
    def __init__(self, id, name, email):
        self.id = id
        self.name = name
        self.email = email

class Product:
    def __init__(self, id, name, price):
        self.id = id
        self.name = name
        self.price = price

class Order:
    def __init__(self, id, customer_id, product_id, quantity):
        self.id = id
        self.customer_id = customer_id
        self.product_id = product_id
        self.quantity = quantity

# Attributes
# Customer: id, name, email
# Product: id, name, price
# Order: id, customer_id, product_id, quantity

# Relationships
# Customer has many orders
# Order belongs to customer
# Product has many orders
# Order belongs to product

%%html
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>mermaid.initialize({startOnLoad:true});</script>
<div class="mermaid">
graph LR;
    subgraph Design_Operations
        SLAs[SLAs];
        Content_Development[Content Development];
        Leads[Leads];
        Orders[Orders];
    end
    subgraph Legal_Design_Services_Startup
        Marketing[Marketing];
        Communication[Communication];
        Opportunity[Opportunity];
        Account[Account];
        Person_Assignee["Person (Assignee)"];
    end
    SLAs --> Content_Development;
    Content_Development --> Leads;
    Leads --> Orders;
    Marketing --> Communication;
    Communication --> Opportunity;
    Opportunity --> Account;
    Account --> Person_Assignee;
</div>
