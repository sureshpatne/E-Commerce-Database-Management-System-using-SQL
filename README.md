# E-Commerce-Database-Management-System-using-SQL
his project focuses on designing and implementing a relational database system for an e-commerce platform using SQL. The goal is to efficiently manage customer information, product catalogs, orders, payments, and inventory while enabling data-driven insights for business growth.
# 🛒 Key Objects for an E‑Commerce Management System
1. Users / Customers
- Customer ID, name, email, phone, address
- Login credentials (username, password, role)
- Order history, wishlist, reviews
2. Products
- Product ID, name, description, category
- Price, stock quantity, SKU
- Images, ratings, discount info
3. Categories
- Category ID, name, description
- Parent/child relationships (for subcategories)
4. Orders
- Order ID, customer ID, order date
- Status (Pending, Shipped, Delivered, Cancelled)
- Payment method, shipping details
  6. Cart
- Cart ID, customer ID
- Products added, quantity, total price
- Temporary storage before checkout
7. Payments
- Payment ID, order ID, customer ID
- Payment method (Card, UPI, COD, Wallet)
- Transaction status
8. Shipping / Delivery
- Shipping ID, order ID
- Address, courier partner, tracking number
- Delivery status
9. Reviews / Ratings
- Review ID, customer ID, product ID
- Rating (1–5), comments, date
# -- Advantages of an E‑Commerce Management System
- 24/7 Availability → Customers can shop anytime, increasing sales opportunities.
- Global Reach → Businesses can serve customers worldwide without physical branches.
- Automation → Orders, payments, and inventory updates happen automatically, reducing manual work.
- Data Insights → Easy tracking of customer behavior, sales trends, and product performance.
- Cost Efficiency → Lower operating costs compared to physical stores (rent, staff, utilities).
- Scalability → Easy to add new products, categories, or expand to new markets.
- Customer Convenience → Quick search, product comparison, and secure checkout improve user experience.
- Integration → Can connect with payment gateways, shipping services, and marketing tools.
# -- Disadvantages of an E‑Commerce Management System
- Security Risks → Vulnerable to hacking, fraud, and data breaches if not well-protected.
- Technical Issues → Downtime, bugs, or slow websites can frustrate customers.
- High Competition → Many online stores compete, making customer retention difficult.
- Logistics Challenges → Shipping delays, damaged goods, or returns can hurt reputation.
- Limited Physical Experience → Customers cannot touch or try products before buying.
- Dependence on Internet → Both customers and businesses rely on stable connectivity.
- Initial Setup Cost → Building a secure, scalable system requires investment in tech and expertise.
- Trust Issues → Some customers hesitate to share payment details online.
# -- Workflow Steps
- Customer Registration
- Customer provides details → stored in Customers table.
- Account Creation
- Bank employee opens savings/current account → entry in Accounts.
- Transactions
- Deposit/withdraw/transfer → recorded in Transactions and balance updated.
- Loan Processing
- Customer applies for loan → stored in Loans with status (Active/Closed).
- Employee Operations
- Employees manage accounts, approve loans, and monitor transactions.
- Reports & Statements
- Generate account summaries, transaction history, and loan reports.
 # -- Step 1: Create  database
      create database
          Ecommerce_Project;
# -- Step 2: use database
         use Ecommerce_Project;
            Database changed

# -- step 3: Create Table Customer 
      mysql> create table Customers(Customer_id int primary key ,Customer_Name varchar(100),Customer_emailid varchar(100),Customer_Phonenumber varchar(20),Customer_Address varchar(40));

# -- Step 4: Create Table Product
    mysql> create table Products(Product_Id int primary key,Product_name varchar(40),Product_Price decimal(11.3),Product_stock int);
    
# -- Step 5: Create Table orders
    mysql> create table Orders (Order_id int primary key ,Customer_id int ,Order_date date ,Total_Amount decimal(11,3) );

# -- Step 6: Create Table orders_items
    mysql> create table Orders_Items(Items_id int primary key , Order_id int ,Product_id int,Quentity int ,Price decimal(11,3));

# -- Step 7: Create Table Payments
    mysql> create table payments(Payment_Id int primary key ,Order_Id int,Payment_date date,Amount decimal(10,2),Payment_mathod varchar(30),constraint fk_payment_order foreign key (order_Id) references orders(order_Id));
# -- Step 8: insert values into Customer Table 
    mysql> insert into Customers values(21,'Shubham','shubhambasole@123',9019074004,'Pune');
    mysql> insert into Customers values(22,'Ramesh','ramesh@123',7854238934,'Bhosari');
    mysql> insert into Customers values (23,'Linga','linga@432',9898987676,'Aundh');
    mysql> insert into Customers values(24,'Rakesh','Rakesh@123',2323234545,'Baner');
    mysql> insert into Customers values(25,'Denesh','denesh@123',9898765644,'Bhalki');
    mysql> insert into Customers values(26,'Akash','akash@123',3345451120,'Benglore');
    mysql> insert into Customers values(27,'Vishnu','vishnu@123',3456542210,'Benglore');
    mysql> insert into Customers values(28,'Ram','ram@133',8989887767,'Kalburgi');
    mysql> insert into Customers values(29,'Sheshank','sheshank@123',7766558987,'Humnbad');
    mysql> insert into Customers values(30,'Omprakash','omprakash@123',8877996667,'Bhaki');
    mysql> insert into Customers values(31,'Omkar','omkar@123',4343238978,'Salapur');
    mysql> insert into Customers values(32,'Omkar','omkar@123',4333221140,'Pune');
    mysql> insert into Customers values(33,'Amar','amar@123',4433225566,'Benglore');
    mysql> insert into Customers values(34,'Aman','aman@123',4433227689,'Belgaon');
    mysql> insert into Customers values(35,'kiran','kiran@123',9033227689,'Sonal');
    
# -- Step 9: insert values into Product Table 
      mysql> insert into products values (41,'Laptops',65000,25);
      mysql> insert into products values (42,'Headphone',1200,20);
      mysql> insert into products values(45,'Pendrive 512GB',4000,40);
      mysql> insert into products values(46,'Smartwatch',2500,10);
      mysql> insert into products values(47,'Power Bank 10000mAh',2099,50);
      mysql> insert into products values(48,'Mobile Bank Cover',499,12);
      mysql> insert into products values(49,'Wireless Earbuds',2999,35);
      mysql> insert into products values(50,'Air Conditioner',40999,51);
      mysql> insert into products values(51,'DSLR Camera',60999,60);
      mysql> insert into products values(52,'Bluetooth Speaker',1599,32);
      mysql> insert into products values(53,'Vireless Mouse',699,90);
      mysql> insert into products values(54,'Laptop Stand',2999,23);
      mysql> insert into products values(55,'Vaccum Cleaner',3099,21);

# -- Step 10: insert values into orders Table
      mysql> insert into orders values (111,22,now(),4000);
      mysql> insert into orders values(112,21,'2025-11-29',25000);
      mysql> insert into orders values (113,25,'2025-11-28',2000);
      mysql> insert into orders values (114,26,'2025-11-26',1000);
      mysql> insert into orders values (115,23,'2025-11-26',6000);
      mysql> insert into orders values (116,24,'2025-11-24',8000);
      mysql> insert into orders values (117,27,'2025-10-23',8000);
      mysql> insert into orders values (118,28,'2025-09-22',9000);
      mysql> insert into orders values (119,30,'2025-10-21',10000);
      mysql> insert into orders values (120,30,'2025-10-22',1099);
      mysql> insert into orders values (121,21,'2025-10-18',599);
      mysql> insert into orders values (122,31,'2025-09-12',899);
      mysql> insert into orders values (123,32,'2025-09-11',1299);
      mysql> insert into orders values (124,34,'2025-09-11',4099);
      mysql> insert into orders values (125,35,'2025-09-10',4099);

# -- step 11: insert values into orders_items Table 
          mysql> insert into order_items values (311,111,41,1)(312,112,42,1),(313,113,43,1),(314,114,44,2),(315,115,45,1),(316,116,46,1),(316,116,46,1),(317,117,47,1),(318,118,48,1),(319,119,49,1),(320,120,50,1),(321,121,51,1),(322,122,52,1),(323,123,53,1),(324,124,54,1),(325,125,55,1),(315,115,45,1),(316,116,46,1),(317,117,47,1),(318,118,48,1),(319,119,49,1),(320,120,50,1),(321,121,51,1),(322,122,52,1),(323,123,53,1),(324,124,54,1),(325,125,55,1);

# -- step 12: insert values into Payments Table 
     mysql> insert into payments  values (212,112, '2025-11-29', 25000, 'Card'),(213,113, '2025-11-28', 2000, 'Cash'),(214,114, '2025-11-26', 1000, 'UPI'),(215,115, '2025-11-26', 6000, 'UPI'),(216,116, '2025-11-24', 8000, 'Card'),(217,117, '2025-10-23', 8000, 'Cash'),(218,118, '2025-09-22', 9000, 'UPI'),(219,119, '2025-10-21', 10000, 'Card'),(220,120, '2025-10-22', 1099, 'UPI'),(221,121, '2025-10-18', 599, 'UPI'),(222,122, '2025-09-12', 899, 'Card'),(223,123, '2025-09-11', 1299, 'UPI'),(224,124, '2025-09-11', 4099, 'UPI'),(225,125,'2025-09-10', 4099, 'Cash');

# -- Conclusion

The E-Commerce Management System provides a structured and efficient approach to managing products, customers, orders, payments, and inventory using MySQL. This project demonstrates key database concepts such as relational design, foreign keys, and data integrity, ensuring accurate and reliable transaction handling. It also shows how SQL queries and stored operations can automate essential e-commerce tasks like order processing, stock updates, and payment tracking.

 


