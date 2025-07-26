Chapter 6: Advanced Inventory Management for Perishables
*********************************************************

For a bakery, inventory management goes far beyond simply counting stock. The perishable nature of both raw ingredients and finished products means that effective inventory control is essential for minimizing waste, ensuring food safety, and maximizing profitability. This chapter covers the advanced Odoo Inventory features that are critical for any food business.

6.1 Warehouse and Location Setup
================================

Odoo's inventory system allows you to model the physical layout of your bakery's storage areas. By default, Odoo creates one warehouse with a standard stock location (WH/Stock). However, you can create a more granular structure to reflect your actual operations. Navigate to **Inventory -> Configuration -> Locations** to create locations such as:
    *   WH/Stock/Dry Goods
    *   WH/Stock/Refrigeration
    *   WH/Stock/Freezer

This detailed location structure helps staff know exactly where to find ingredients and allows for more precise inventory tracking.[21]

6.2 Enabling and Using Lot Tracking and Expiration Dates
=========================================================

Traceability is not an optional feature for a food business; it is a fundamental requirement for quality control and food safety. Odoo's lot tracking capability allows you to trace a batch of ingredients from the moment it is received from a supplier, through the manufacturing process, and all the way to the final sale. This is invaluable in the event of a product recall.

The configuration process is straightforward:
    1.  **Enable Features**: Go to **Inventory -> Configuration -> Settings**. In the **Traceability** section, check the boxes for **Lots & Serial Numbers** and **Expiration Dates**.[28]
    2.  **Configure Products**: For each perishable product (both raw materials like cream and finished goods like cakes), open its product form. Go to the **Inventory** tab and set the **Tracking** field to **By Lots**.[29]
    3.  **Set Expiration Times**: On the same tab, under the **Dates** section, you can define the product's shelf life. For example, for "Fresh Cream," you might set the **Expiration Time** to 7 days. This tells Odoo to automatically calculate the expiration date as 7 days from the date of receipt.[28]

With this configuration in place, whenever you receive a shipment of a tracked item, Odoo will require the user to enter a **Lot Number** (which can be the supplier's batch number or one you generate internally) and will automatically suggest an expiration date. This creates a complete traceability record for every batch of perishable goods.[28]

.. image:: /images/chapter6/lot_number_receipt.png
   :alt: Odoo's detailed operations pop-up for entering a lot number and expiration date upon receipt.

6.3 Configuring Removal Strategies: First-Expired-First-Out (FEFO)
====================================================================

To minimize waste, it is crucial that the ingredients closest to their expiration date are used first. Manually tracking this can be tedious and prone to error. Odoo automates this critical process through **Removal Strategies**.

The most important strategy for a bakery is **First-Expired-First-Out (FEFO)**. By applying this strategy to your stock locations, you instruct Odoo to always suggest picking the lot of an ingredient that has the earliest expiration date. For example, when a baker starts a manufacturing order for croissants, Odoo will automatically reserve the batch of butter that is set to expire soonest, ensuring it gets used before it spoils.[30, 31]

To configure this, navigate to **Inventory -> Configuration -> Locations**. Select the location where your perishable ingredients are stored (e.g., WH/Stock/Refrigeration) and set its **Removal Strategy** to **First Expired, First Out (FEFO)**.[31, 32] This simple configuration automates a vital business process that directly impacts the bakery's bottom line by reducing waste.

6.4 Automating Replenishment with Reordering Rules
====================================================

Preventing stock-outs of key ingredients is essential to keep production running smoothly. Odoo's **reordering rules** automate the replenishment process by monitoring stock levels and triggering purchase orders when quantities fall below a predefined minimum.[5]

For each critical ingredient, you can set up a reordering rule under **Inventory -> Configuration -> Reordering Rules**. The key fields are:
    *   **Product**: The ingredient to monitor.
    *   **Min Quantity**: The minimum stock level. When the forecasted quantity drops below this number, the rule is triggered.
    *   **Max Quantity**: The desired stock level to replenish to.

For example, you could set a rule for "Yeast" with a minimum of 1kg and a maximum of 5kg. If a production order consumes yeast and the forecasted stock drops to 0.9kg, Odoo will automatically create a draft Request for Quotation (RFQ) for the default vendor for 4.1kg of yeast, bringing the stock back up to the maximum level.[20, 33] This ensures you never run out of essential items unexpectedly.
