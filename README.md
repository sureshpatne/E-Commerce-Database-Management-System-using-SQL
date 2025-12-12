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
 # -- Step 1: Create and use database
 


