Chapter 8: The Heart of the Bakery: Point of Sale (POS) Setup
*************************************************************

The Point of Sale is the primary interface for customer interaction in most bakeries. An efficient, reliable, and easy-to-use POS system is critical for providing excellent customer service and ensuring smooth operations, especially during busy periods. Odoo's POS is fully integrated with inventory and accounting, providing a seamless flow of information from the front counter to the back office.

8.1 Configuring Your POS Interface and Hardware
===============================================

The first step is to create a POS profile for your shop. Navigate to **Point of Sale -> Configuration -> Point of Sale** and create a new record for your bakery. Here you can define various settings, such as whether it is a bar/restaurant (which enables table management) or a standard shop.[40]

The main POS screen is organized by product categories. As configured in Chapter 4, these categories will appear as tabs, allowing cashiers to quickly find items.[5] You can also connect essential hardware to your POS system, including:
    *   **Receipt Printers**: For printing customer receipts.
    *   **Cash Drawers**: That open automatically upon a cash transaction.
    *   **Barcode Scanners**: To quickly add packaged items to an order.
    *   **Scales**: For items sold by weight.[1, 41]

8.2 Setting Up Payment Methods
==============================

You must configure all the payment methods your bakery accepts. This is done under **Point of Sale -> Configuration -> Payment Methods**. You can create methods for:
    *   **Cash**: The most common method.
    *   **Credit/Debit Cards**: For card payments.
    *   **Customer Account**: For wholesale customers who pay on account.

A critical step in this configuration is linking each payment method to an **Accounting Journal**. For example, the "Cash" payment method should be linked to your "Cash Journal," and the "Credit Card" method should be linked to your "Bank Journal." This ensures that when a payment is processed in the POS, the transaction is recorded correctly in your financial books, automating a significant portion of your bookkeeping.[42, 43, 44, 45]

.. image:: /images/chapter8/pos_payment_methods.png
   :alt: The configuration screen for POS Payment Methods in Odoo, showing the link to an accounting journal.

8.3 Managing a POS Session
==========================

The daily workflow for a cashier is managed within a POS session.
    1.  **Open Session**: At the start of the day, the cashier opens a new session from the POS dashboard. They will be prompted to enter the starting cash amount in the drawer (the opening cash balance).
    2.  **Process Orders**: Throughout the day, the cashier adds products to the cart, selects a customer if applicable, and proceeds to the payment screen to accept payment.
    3.  **Cash In/Out**: If cash needs to be added or removed from the drawer during the day (e.g., for a petty cash expense), the cashier can use the "Cash In/Out" feature to record the transaction.
    4.  **Close Session**: At the end of the day, the cashier closes the session. They will be prompted to count the cash in the drawer. Odoo will then display a closing summary, showing the total sales by payment method and any expected cash difference. Upon closing, all transactions are posted to the accounting journals.[46]

8.4 Advanced POS: Loyalty Programs, Promotions, and Custom Orders
===================================================================

Odoo's POS can be extended to handle more advanced retail scenarios common in bakeries.
    *   **Loyalty Programs**: Encourage repeat business by creating a loyalty program under **Point of Sale -> Configuration -> Loyalty Programs**. You can set up rules to award customers points for their purchases, which they can later redeem for rewards or discounts.[5, 47]
    *   **Promotions & Discounts**: Easily create promotions like "10% off all pastries on Tuesdays" or "Buy a coffee, get a croissant for $1" using the **Promotions** feature. These discounts are applied automatically at the POS when the conditions are met.[48]
    *   **Custom Orders**: Bakeries frequently handle special requests, such as writing "Happy Birthday" on a cake or accommodating a dietary restriction (e.g., "no nuts").[49] While Odoo's standard POS can handle predefined options using product variants, it is less suited for unique, one-off requests. For bakeries that do a significant amount of custom cake orders, it is highly recommended to use a specialized third-party module from the Odoo App Store. Modules like "Odoo POS Order Customization" allow cashiers to add notes to specific order lines or answer a series of questions (e.g., "What message to write on the cake?"). These notes can be printed on the kitchen receipt, ensuring the bakers have the correct instructions, and can even add an upcharge for the customization.[50, 51]
