# MIST4610-Group-5-Project-1
#Team members:
1. Zhen, Christina - 811674601 - https://github.com/cz67968/MIST4610-Group-5-Project-1
2. Snow, Luke -
3. Arfath, Rushil - 811460339 - https://github.com/R1Arafath/Group-5-Project-1-Final
4. Khan, Azaan - 811686335 - https://github.com/Azaank09/group-project/tree/main
5. Fontoura, Gabriel - 811794390

# Problem Description:
Our project focuses on creating a database for an online bookstore to efficiently track key business operations, including sales, employee hours, genres, authors, and inventory management. The database is designed to manage book inventory by categorizing books under a one-to-many relationship, where multiple ISBNs can belong to a single category. Sales transactions are recorded through a many-to-many relationship between books and sales, using a weak entity that links sales details with inventory. This structure allows for tracking which books are sold in each transaction. Additionally, employee work hours are managed through another many-to-many relationship between employees and shifts, where each employee can work multiple shifts, and each shift can have multiple employees. By structuring the database in this way, the system provides an organized method for analyzing book sales, tracking employee work schedules, and ensuring efficient inventory management.

# Data Model:

![421644134-0ea972b7-c4b5-4603-aed1-3760d04fb12c](https://github.com/user-attachments/assets/b30cb57f-debb-471e-9a89-9afcfa47e6bb)


Our team’s data model is designed for an online bookstore, capturing key relationships between sales, inventory, employees, and shifts. The inventory entity tracks books, linking each book to a specific category through a one-to-many relationship, as multiple books can belong to a single category. Sales transactions are recorded through a many-to-many relationship between sales and inventory using the sales details entity, which connects each sale to the books purchased. Since a sale can include multiple books, and a book can appear in multiple sales, this entity ensures proper tracking of transactions. Employee work hours are managed through another many-to-many relationship between employees and shifts, where an employee can work multiple shifts, and a shift can have multiple employees. The shift assignment entity facilitates this relationship by linking employees to specific shifts. The sales entity serves as the foundation of the model, containing key transaction data and connecting to shifts through employee sales records. This data model allows for efficient tracking of inventory, sales trends, and employee scheduling, optimizing bookstore operations.

# Data Dictionary:
![421649199-7c2671ee-c530-4922-bbdc-157854272f8f](https://github.com/user-attachments/assets/39d87381-d688-4bea-bae8-5437ff753407)
![421649921-094aeadc-79fe-46b9-a02d-d8f1f3eb9127](https://github.com/user-attachments/assets/b81cf3f6-996e-4098-8f39-adc3b332bf4a)
![421651177-12fed416-d2bd-4f37-ba00-c5ccfadae4f6](https://github.com/user-attachments/assets/d79276ae-f8dd-4e3b-a7a8-b5b988d7109f)
![421651456-a2cc3d2f-5b10-4722-a4db-b6f0f17d87c1](https://github.com/user-attachments/assets/323fdd13-d4a5-4c27-b915-7ddbe6430830)
![421651724-d991d994-3ba6-4bb0-9104-485ceb5a9d0a](https://github.com/user-attachments/assets/6123ce1c-230a-4ca9-9228-1aff51b3fb92)
![421652136-f02bc27e-2835-4e27-94aa-4747da52d601](https://github.com/user-attachments/assets/d8ae51ae-b7a9-4fe5-b504-b37bf23ca6f3)
![421652438-6791fb3c-3551-4586-bed8-679594dd89e9](https://github.com/user-attachments/assets/27cfa026-849f-4c02-95bd-a1688533dac0)


# Queries:
Query 1 retrieves employee details, assigned shifts, and pay rates by joining multiple tables to link employees, assignments, and shifts for a comprehensive view.

![422522538-2aa7443a-ec97-45a3-bb84-1584c172d02b](https://github.com/user-attachments/assets/f1075cfa-2451-495c-9227-6542ff4afe26)


Description: This query retrieves the total number of books sold by each employee, ordering them from highest to lowest sales. This helps evaluate employee performance and identify top sellers.

Query 2 displays each book's selling price, purchase cost, and computed profit, helping identify high-margin books that contribute the most to revenue.

![422523402-a72d8090-7c38-47ca-86d9-7e87fe3cd310](https://github.com/user-attachments/assets/8905ea5a-2de4-4115-a185-9a8abee330b1)


Description: This query highlights books with higher-than-average profit, helping recognize best-selling, high-margin products to inform purchasing and marketing strategies.

3.Query 3 identifies how much profit each book generates per sale, helping assess which books contribute the most profit.

![422523685-0d13c720-374c-4507-b5fb-4053fb5af2b5](https://github.com/user-attachments/assets/86ff40e5-bc03-4338-bd9c-ffd5df68bad3)


Description: This query highlights the most sold books along with their price and profitability. It supports restocking decisions and provides insight into customer preferences.

Query 4 retrieves sales data, including product details, pricing, and quantity sold, using a window function to compute total profit across all sales. It joins sales data with inventory to link product details and transactions.

![422523945-03b3f3fd-2b19-45d2-8598-cedb4b57e3d9](https://github.com/user-attachments/assets/d36eeee7-3c3c-49d9-aa0a-fbcf9f513008)


Description: This query calculates the total hours worked by each employee and ranks them from highest to lowest. It helps with payroll processing and identifying employees with the highest workload.

Query 5 retrieves book details, including ISBN, title, author, available quantity, genre categorization, and aisle assignment. It joins the inventory table with the category table to link books with their respective categories.

![422524188-e6b3ceb4-dd46-482e-a7e4-fae8fc547099](https://github.com/user-attachments/assets/7c864c26-40f8-48eb-ad79-975c22d062f3)


Description: This query calculates profit per book (ISBN) and the total profit of each sale transaction, supporting financial analysis and revenue tracking.

Query 6 provides employee shift details, labor per employee, and total labor cost per shift by calculating payroll based on hours and pay rate, using window functions for total shift labor.

![422530926-7205f4d4-b9af-4c83-bb38-af7fce816ec1](https://github.com/user-attachments/assets/035a7407-f14f-4c2c-8d9e-f3cb1d1bab05)


Description: This query provides payroll calculations per employee shift and the total labor cost per shift. It assists in budgeting and staffing decisions.

Query 7 calculates the total profit generated over the entire sales period by computing profit per sale and using a window function to sum total profit across all transactions.

![422531375-a4a013c3-fce2-4299-afe2-8050a6e5c395](https://github.com/user-attachments/assets/db662cd8-3685-449f-a75c-13b3f8296110)


Description: This query calculates the total profit generated over all sales transactions. It is useful for high-level financial reporting and performance analysis.

Query 8 retrieves the employee with the earliest start date, indicating the longest tenure in the company.

![422531683-3efaea1b-0283-4b99-a61f-f077a5103939](https://github.com/user-attachments/assets/5b57fa29-ab92-4210-bbec-b49e26ffb817)


Description: This query finds the employee with the longest tenure in the company. It can be used for employee recognition programs or for workforce planning.

Query 9 calculates labor cost per employee shift and uses a window function to compute the total labor cost across all shifts over the entire sales period.

![422532038-223a4fbc-0ecf-4b2e-a7fe-e1caf684df86](https://github.com/user-attachments/assets/8ca3fb73-3efc-43ef-8a0f-ce5df4c8dc8d)


Description: This query computes the total labor cost for all shifts over the entire sales period. It is useful for financial planning and workforce cost analysis.

Query 10 retrieves book inventory details, including ISBN, title, author, available quantity, category name, and aisle location by joining the inventory and category tables.

![422532359-ba5be8cd-cc2c-4c80-a0e6-01d7d3e33ed3](https://github.com/user-attachments/assets/716ed9c9-d91a-4a4b-887b-b2989528f2a7)


Description: This query retrieves book inventory details, including quantity available and location in the store. It is helpful for stock management and customer assistance.

# Database Information:

![422532611-55392353-a833-40ed-8fde-53a91ce5f930](https://github.com/user-attachments/assets/3ebf2a07-655c-4493-955d-0d521fa872e5)


