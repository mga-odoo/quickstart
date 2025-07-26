Chapter 5: Procurement and Supplier Management
************************************************

Effective procurement is the foundation of a successful bakery. Ensuring a consistent supply of high-quality raw materials at the right price is critical. Odoo's Purchase application streamlines the entire procurement process, from managing supplier information to receiving and paying for goods.

5.1 Setting Up Vendors and Purchase Pricelists
===============================================

The first step is to create a complete record for every supplier the bakery works with. Navigate to the **Purchase** app and click on **Orders -> Vendors**. Click **Create** to add a new vendor, filling in their contact details and payment information.

To streamline the ordering process, you can configure vendor pricelists. On the product form for a raw material (e.g., "All-Purpose Flour"), go to the **Purchase** tab. Here, you can add a line under the **Vendors** section, selecting a supplier and entering the price they charge for that specific item. If you have multiple suppliers for the same ingredient, Odoo will use the first one in the list as the default when generating a purchase order. This feature saves time and reduces the risk of data entry errors during procurement.[27]

5.2 The Purchase-to-Pay Workflow
=================================

The standard procurement workflow in Odoo is a structured process designed for clarity and control. It moves from a draft request to a confirmed order, followed by receipt of goods and payment of the bill.
    1.  **Create a Request for Quotation (RFQ)**: The process begins by creating an RFQ in the **Purchase** app. Select the vendor, add the products (ingredients) you wish to order, and specify the quantities. At this stage, it is simply a draft document.[27]
    2.  **Confirm Order**: Once you are ready to place the order, click the **Confirm Order** button. The RFQ's status changes to **Purchase Order (PO)**, and it becomes a legally binding document. You can then send the PO to your vendor directly from Odoo via email.
    3.  **Receive Products**: When the supplier delivers the goods, a **Receipt** button will be visible on the PO. Clicking this will take you to the corresponding incoming shipment record in the Inventory app. Here, you will verify the quantities received.
    4.  **Create Bill**: After receiving the goods and the supplier's invoice, you can create a vendor bill directly from the PO. This ensures that the bill is accurately matched to the goods and prices that were ordered. The bill is then managed in the Accounting app for payment.

.. image:: /images/chapter5/purchase_order_flow.png
   :alt: Diagram of the Odoo Purchase Order workflow from RFQ to Bill.

5.3 Receiving and Verifying Raw Material Shipments
====================================================

The physical receipt of goods is a critical inventory transaction. When a delivery arrives from a supplier, the warehouse staff will process it in the **Inventory** app. They will find the incoming transfer that corresponds to the purchase order and validate the quantities received against what was ordered. Upon validation, Odoo automatically increases the on-hand stock levels for those raw materials, making them available for production.[21]

Once the receipt is validated, the accounting department can proceed with creating the vendor bill from the purchase order. This bill will then enter the accounts payable workflow, where it will be approved and scheduled for payment according to the agreed-upon terms with the supplier.[18]
