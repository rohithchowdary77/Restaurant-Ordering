# Andhra Ruchulu: Restaurant Ordering System

A comprehensive **Java Swing** application designed for both restaurant management and customer self-service. The system features a dual-interface for Administrators and Customers, backed by a persistent **MySQL** database for secure authentication and real-time menu storage.

---

## 🛠️ Tech Stack
* **Frontend:** Java Swing GUI.
* **Styling:** Custom `Graphics2D` gradients with "Poppins", "Arial", or "Segoe UI" typography.
* **Backend:** MySQL Database.
* **Connectivity:** JDBC (Java Database Connectivity).

---

## 🚀 Key Features

### 1. Authentication & Role Management
* **Multi-Role Login:** Supports distinct workflows and permissions for **Admin** and **Customer** roles.
* **User Registration:** New users can be registered directly into the system database.
* **Secure Access:** Validates credentials (username, password, and role) against stored records.

### 2. Admin Dashboard (Menu Management)
* **Real-time CRUD:** Administrators can **C**reate, **R**ead, **U**pdate, and **D**elete menu items (Name, Price, and Category).
* **Automated Tracking:** Menu items are automatically tracked and ordered via unique database IDs.
* **Interactive UI:** Utilizes a `JTable` with selection listeners to quickly populate fields for rapid editing or deletion.

### 3. Customer Ordering Flow
* **Category Browsing:** Navigation through specific categories: *Starter, Main Course, Dessert,* and *Juice*.
* **Quantity Selection:** Includes a custom `JSpinnerEditor` for selecting item quantities directly within the menu table.
* **Cart Persistence:** Maintains a session-based `ArrayList` of selected items as the customer navigates different menu sections.

### 4. Billing & Receipts
* **Table Assignment:** Requires a table number to proceed with order finalization.
* **Detailed Receipts:** Generates a formatted text-based bill in a `JTextArea` including:
    * Itemized breakdown (Name, Qty, Price, Total).
    * Grand Total calculation.
    * Restaurant contact and branding information.

---

## 📂 System Architecture

| Component | Responsibility |
| :--- | :--- |
| **`RestaurantOrderingSystem`** | Main entry point; initializes DB connection and launches the Login page. |
| **`Page` & `Page$1`** | Base templates for consistent UI styling, gradients, and custom components. |
| **`LoginPage`** | Manages user authentication and registration logic. |
| **`AdminPage`** | Provides the interface for menu management and database updates. |
| **`CustomerPage`** | Displays category-specific menus and handles "Add to Cart" actions. |
| **`BillPage`** | Processes orders, calculates final costs, and displays the receipt. |
| **`JSpinnerEditor`** | Custom table cell editor for numerical quantity input. |

---


---

## 🚦 How to Run
1.  **Database Setup:** Run the SQL commands provided above in your MySQL workbench.
2.  **Configuration:** Ensure your MySQL credentials match the driver settings (Default: User `root`, Password `Nrc@2006`).
3.  **Dependencies:** Ensure the `mysql-connector-java` JAR is present in your project classpath.
4.  **Execution:** Run the `RestaurantOrderingSystem` class to start the application.
