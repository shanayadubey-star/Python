# Python Dynamic Billing System

## 1. Project Overview

The Python Dynamic Billing System is a console-based application developed using Python. It is designed to simplify and automate basic billing operations for small businesses and retail shops.

The application allows users to manage products, maintain a shopping cart, calculate bills, apply discounts, calculate GST, and generate customer invoices.

The system provides a menu-driven interface through which users can perform different billing operations without manually calculating product prices, quantities, discounts, or taxes.

The application uses Python's built-in data structures such as dictionaries and lists to manage product information, cart details, and invoice history. No external database is required.

## 2. Project Objectives

The main objectives of this project are:

- To automate the basic billing process.
- To reduce manual calculation errors.
- To manage product details efficiently.
- To calculate product-wise and total purchase amounts.
- To apply discounts and GST automatically.
- To generate structured customer invoices.
- To maintain invoice history during application execution.
- To provide a simple and user-friendly console interface.

## 3. Technologies Used

| Technology | Purpose |
|---|---|
| Python 3 | Core programming language |
| Dictionaries | Store product and customer information |
| Lists | Manage shopping cart and invoice history |
| Decimal | Perform accurate monetary calculations |
| Functions | Organize application functionality |
| Datetime | Generate invoice date and time |
| Command Line Interface | User interaction |

**External Dependencies:** None.

**Database:** Not used. Application data is maintained in memory.

## 4. Project Modules

### 4.1 Product Management

This module manages product-related operations.

Functionalities:
- Add new products.
- Display available products.
- Update product names and prices.
- Delete products.
- Assign unique product IDs automatically.

Each product contains:
- Product ID
- Product Name
- Product Price

### 4.2 Shopping Cart Management

This module manages products selected by customers.

Functionalities:
- Add products to the cart.
- View cart details.
- Update product quantities.
- Remove products from the cart.
- Automatically calculate individual product amounts.

The system checks whether a product already exists in the cart. If it does, the quantity is increased instead of creating a duplicate entry.

### 4.3 Customer Management

During checkout, the application collects customer information.

Customer details include:
- Customer Name
- Customer Phone Number

These details are displayed on the generated invoice.

### 4.4 Billing and Calculation

This module calculates the final payable amount.

The billing process includes:

1. Calculate subtotal.
2. Calculate discount amount.
3. Calculate taxable amount.
4. Calculate GST.
5. Calculate final payable amount.

**Billing formulas:**

Subtotal:

`Subtotal = Sum(Product Price × Quantity)`

Discount:

`Discount = Subtotal × Discount Percentage / 100`

Taxable Amount:

`Taxable Amount = Subtotal - Discount`

GST:

`GST = Taxable Amount × GST Percentage / 100`

Grand Total:

`Grand Total = Taxable Amount + GST`

### 4.5 Invoice Generation

After successful checkout confirmation, the application generates a customer invoice.

Invoice details include:
- Unique invoice number.
- Invoice generation date and time.
- Customer information.
- Purchased product details.
- Product prices and quantities.
- Subtotal.
- Discount.
- GST.
- Final payable amount.

### 4.6 Invoice History

This module maintains a list of generated invoices during the current application session.

Users can view:
- Invoice number.
- Customer name.
- Invoice date.
- Total bill amount.

## 5. Application Workflow

The application follows the below workflow:

1. Start the billing application.
2. Display the main menu.
3. Add and manage products.
4. Select products for customer purchases.
5. Add selected products to the shopping cart.
6. Update or remove cart items if required.
7. Enter customer information.
8. Enter discount and GST percentages.
9. Calculate the final bill.
10. Confirm invoice generation.
11. Display the customer invoice.
12. Store the invoice in session history.
13. Return to the main menu for the next transaction.

## 6. Functional Requirements

| Requirement ID | Description |
|---|---|
| FR-01 | The system shall allow users to add products. |
| FR-02 | The system shall display all available products. |
| FR-03 | The system shall allow users to update product details. |
| FR-04 | The system shall allow users to delete products. |
| FR-05 | The system shall allow users to add products to a cart. |
| FR-06 | The system shall allow users to update cart quantities. |
| FR-07 | The system shall calculate product-wise amounts. |
| FR-08 | The system shall calculate discounts. |
| FR-09 | The system shall calculate GST. |
| FR-10 | The system shall generate customer invoices. |
| FR-11 | The system shall maintain invoice history during execution. |
| FR-12 | The system shall validate user inputs. |

## 7. Non-Functional Requirements

- **Usability:** Simple menu-driven console interface.
- **Performance:** Fast execution for small product catalogs and transactions.
- **Reliability:** Input validation to prevent common invalid entries.
- **Maintainability:** Modular functions for different billing operations.
- **Accuracy:** Decimal-based calculations for monetary values.
- **Portability:** Can run on Windows, Linux, and macOS with Python 3.

## 8. Input Validation and Error Handling

The application includes validation to improve reliability.

Examples:
- Product names cannot be empty.
- Product prices must be greater than zero.
- Product quantities must be positive integers.
- Discount percentages cannot exceed 100%.
- GST percentages cannot exceed 100%.
- Invalid product IDs are rejected.
- Invalid numerical inputs are handled.
- Empty shopping carts cannot be checked out.

## 9. Advantages

- Easy to understand and operate.
- No database setup required.
- No external package installation required.
- Reduces manual billing calculations.
- Supports multiple products in one transaction.
- Provides automatic discount and GST calculations.
- Can be extended into a desktop or web application.

## 10. Current Limitations

The current implementation is designed as a basic billing application.

Limitations include:

- Product information is not permanently stored.
- Invoice history is lost when the application closes.
- Generated invoices are displayed only in the console.
- No inventory or stock management.
- No login or user authentication.
- No payment gateway integration.
- GST is entered manually and does not automatically determine CGST, SGST, or IGST.

## 11. Future Enhancements

The application can be enhanced with the following features:

1. SQLite or MySQL database integration.
2. PDF invoice generation.
3. Graphical user interface using Tkinter.
4. User authentication for admin and cashier.
5. Product inventory and stock management.
6. Customer purchase history.
7. Sales reports and analytics.
8. Multiple GST tax categories.
9. Payment mode integration.
10. Daily, weekly, and monthly sales summaries.

## 12. Conclusion

The Python Dynamic Billing System demonstrates the practical implementation of Python programming concepts such as functions, dictionaries, lists, loops, conditional statements, exception handling, and data validation.

It provides a simple and effective solution for managing basic billing operations, calculating taxes and discounts, and generating customer invoices.

The project also provides a foundation for developing a more advanced billing application with database integration, graphical interfaces, inventory management, and reporting capabilities.
