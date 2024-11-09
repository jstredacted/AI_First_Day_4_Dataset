# Restaurant Orders Dataset - Metadata

This document provides a description of the columns and data structure for the **Restaurant Orders Dataset**. This dataset contains information about customer orders, including order details, meal information, payment status, and delivery/pickup times.

## Table of Contents
1. [Dataset Overview](#dataset-overview)
2. [Column Descriptions](#column-descriptions)
3. [Data Usage Examples](#data-usage-examples)

## Dataset Overview
The **Restaurant Orders Dataset** is used to track customer orders in a restaurant, including meal orders, quantities, prices, total amount, and the order's payment status. It helps restaurants manage orders, track revenue, optimize menu recommendations, and improve customer service.

## Column Descriptions

### 1. **Order ID**
   - **Description**: A unique identifier for each order placed in the restaurant.
   - **Data Type**: String (Alphanumeric)
   - **Example**: "O001", "O002"
   - **Notes**: The `Order ID` is sequential and automatically generated for each new order.

### 2. **Customer Name**
   - **Description**: The name of the customer who placed the order.
   - **Data Type**: String (Text)
   - **Example**: "Alice Green", "Bob White"
   - **Notes**: The customer's full name is provided.

### 3. **Customer Contact**
   - **Description**: The contact number of the customer.
   - **Data Type**: String (Phone number format)
   - **Example**: "555-1234", "555-5678"
   - **Notes**: The contact number is given in a standardized phone number format (e.g., "555-xxxx").

### 4. **Meal Ordered**
   - **Description**: The name of the meal ordered by the customer.
   - **Data Type**: String (Text)
   - **Example**: "Burger", "Pizza", "Pasta", "Steak", "Salad"
   - **Notes**: This field lists the type of food item selected by the customer.

### 5. **Quantity**
   - **Description**: The quantity of the meal ordered by the customer.
   - **Data Type**: Integer
   - **Example**: 1, 2, 3
   - **Notes**: This field indicates how many servings of a specific meal were ordered.

### 6. **Price per Unit ($)**
   - **Description**: The cost of a single unit of the ordered meal.
   - **Data Type**: Decimal (Currency)
   - **Example**: 8.50, 12.00
   - **Notes**: The price per meal is recorded in dollars and cents. This value is set by the restaurant.

### 7. **Total Amount ($)**
   - **Description**: The total cost of the order (calculated as Quantity × Price per Unit).
   - **Data Type**: Decimal (Currency)
   - **Example**: 17.00, 24.00
   - **Notes**: This field stores the total amount spent on each order. It is calculated by multiplying the quantity of meals ordered by their respective prices.

### 8. **Payment Status**
   - **Description**: The status of the payment for the order.
   - **Data Type**: String (Categorical)
   - **Example**: "Paid", "Pending"
   - **Notes**: This field indicates whether the payment for the order has been successfully processed or is still pending.

### 9. **Order Date**
   - **Description**: The date on which the order was placed by the customer.
   - **Data Type**: Date (YYYY-MM-DD)
   - **Example**: "2024-11-01", "2024-11-02"
   - **Notes**: The order date is when the customer finalized their order, often recorded in local time.

### 10. **Delivery/Pickup Date**
   - **Description**: The date when the order is either delivered to the customer or is ready for pickup.
   - **Data Type**: Date (YYYY-MM-DD)
   - **Example**: "2024-11-01", "2024-11-02"
   - **Notes**: This field records the expected or actual delivery/pickup date for the meal.

---

## Data Usage Examples

### 1. **Customer Analytics**
   - Understanding customer behavior by analyzing the types of meals ordered, their frequency, and the amount spent.
   
### 2. **Revenue Forecasting**
   - Using total amounts and order counts to predict revenue and help with sales forecasting.

### 3. **Order Management**
   - Tracking the delivery status of orders to ensure timely service and avoid delays.

### 4. **Payment Management**
   - Monitoring orders with pending payments for follow-up actions.

### 5. **Promotions and Offers**
   - Personalizing marketing campaigns based on customer preferences, order history, and frequency of meals ordered.

---

## Additional Information

- **Primary Key**: `Order ID` – Unique identifier for each order.
- **Foreign Keys**: None – This dataset is self-contained; however, it could be linked to other datasets (e.g., customer details, restaurant inventory).
- **Missing Values**: It is possible to encounter missing or incomplete values for fields like "Delivery/Pickup Date" if the order is still pending.
- **Date Range**: The `Order Date` and `Delivery/Pickup Date` should fall within the operational dates of the restaurant, which might be daily or seasonal.
- **Data Constraints**: 
  - The `Quantity` must always be a positive integer.
  - The `Price per Unit ($)` and `Total Amount ($)` must always be positive decimal values, reflecting real-world pricing.
  - `Order Date` and `Delivery/Pickup Date` should always be valid dates in the future or past depending on the specific situation.

---

## License

This dataset is intended for use within restaurant operations, data analysis, and machine learning applications. Proper permissions must be obtained if the data includes personally identifiable information or if used for commercial purposes.
