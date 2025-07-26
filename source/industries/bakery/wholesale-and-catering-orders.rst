Chapter 9: Managing Wholesale and Catering Orders
*****************************************************

In addition to retail sales, many bakeries have a significant B2B business, supplying goods to local cafes, restaurants, or catering corporate events. These transactions are typically larger, may involve special pricing, and are managed through the Odoo **Sales** application rather than the POS.

9.1 The Quote-to-Cash Process for B2B Customers
================================================

The workflow for a wholesale or catering order is more formal than a retail transaction and is designed to handle negotiations and credit terms.
    1.  **Create Quotation**: The process begins in the **Sales** app by creating a quotation for the client. The quotation details the products, quantities, prices, and any specific terms.[48, 52]
    2.  **Send Quotation**: The quotation can be sent to the client directly from Odoo as a professional-looking PDF. Clients can even view and approve the quotation online through a customer portal link.
    3.  **Confirm to Sales Order**: Once the client accepts the quotation, it is confirmed into a **Sales Order**. This action is the trigger for the fulfillment process. Odoo automatically creates a **Delivery Order** in the Inventory app to schedule the shipment of goods and prepares a draft **Invoice** in the Accounting app.[53]
    4.  **Deliver & Invoice**: The bakery staff will process the delivery order to ship the goods. The invoice can then be sent to the client for payment according to the agreed-upon terms (e.g., Net 30 days).

9.2 Creating and Managing Wholesale Pricelists
===============================================

Wholesale customers typically receive preferential pricing compared to retail customers. Odoo's **Pricelists** feature automates this. You can create a "Wholesale Pricelist" that applies a specific discount (e.g., 20% off the public price) or sets fixed prices for certain items.

This pricelist can then be assigned to your wholesale customer's contact record. When you create a new quotation for that customer, Odoo will automatically apply the wholesale pricelist, ensuring that the pricing is always accurate and consistent without requiring manual adjustments by the sales staff.[48]
