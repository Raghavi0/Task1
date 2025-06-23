Domain name: E-Commerce 





| Relationship        | Description                                       |
| ------------------- | ------------------------------------------------- |
| Customer ↔ Order    | One customer can place many orders (1:M)         |
| Order ↔ OrderItem   | One order can have many order items (1:M)        |
| Product ↔ OrderItem | One product can appear in many order items (1:M) |
| Order ↔ Payment     | One order has one payment (1:1)                   |
| Order ↔ Shipping    | One order has one shipping record (1:1)           |
| Product ↔ Category  | One category can contain many products (1:M)     |
| Customer ↔ Review   | One customer can write many reviews (1:M)        |
| Product ↔ Review    | One product can have many reviews (1:M)          |


Entity :
1.Customer
CustomerID (PK)
Name, Email, Phone, Address
2.Product
ProductID (PK)
Name, Description, Price, StockQuantity, CategoryID (FK)
3.Category
CategoryID (PK)
CategoryName, Description
4.Order
OrderID (PK)
CustomerID (FK), OrderDate, Status, TotalAmount
5.OrderItem
OrderItemID (PK)
OrderID (FK), ProductID (FK), Quantity, Price
6.Payment
PaymentID (PK)
OrderID (FK), PaymentDate, Amount, PaymentMethod, PaymentStatus




Primary Key :is a unique identifier for each record in a table. It ensures that no two rows have the same value and cannot be null.

Foreign Key: is a field in one table that refers to the **Primary Key** in another table. It is used to establish a relationship between two tables.
