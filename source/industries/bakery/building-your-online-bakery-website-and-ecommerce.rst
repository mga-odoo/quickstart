Chapter 10: Building Your Online Bakery: Website and eCommerce
**************************************************************

An online presence is essential for the modern bakery, providing an additional sales channel and a platform to showcase products. Odoo's integrated **Website** and **eCommerce** applications allow you to build and manage a professional online store that is directly connected to your inventory and order management systems.

10.1 Using the Odoo Website Builder
====================================

Odoo's website builder is designed to be incredibly user-friendly, allowing you to create a beautiful website without writing a single line of code. It uses a drag-and-drop interface with pre-designed building blocks. You can easily add text blocks, image galleries, contact forms, and more. Odoo even offers an AI-based website generator that can create an initial design for you based on your industry and preferred style.[5, 21, 54, 55]

10.2 Configuring Products for Online Sales
===========================================

Any product created in Odoo can be sold online with a single click. On the product form, simply switch the **Published** toggle in the top right corner. The product will then appear in your online store.

For products with variants, such as cakes with different sizes and flavors, the product configurator will automatically appear on the eCommerce product page. This allows customers to select their desired options before adding the item to their cart, with the price updating in real-time based on their selections.[5] This provides a seamless online experience that is directly linked to the same product variant structure used in the POS.

10.3 Setting Up Online Payment Acquirers
=========================================

To accept payments online, you need to integrate with one or more payment gateways. Odoo supports a wide range of payment acquirers out of the box, including major providers like Stripe and PayPal.

Configuration is done under **Website -> Configuration -> Payment Acquirers**. You will need to enter your account credentials for the chosen provider. Once enabled, the payment option will appear on your website's checkout page, allowing customers to pay securely with their credit cards.[5, 21, 56, 57]

10.4 Managing Online Orders: Click-and-Collect and Local Delivery
===================================================================

A key advantage of Odoo's integrated eCommerce is the ability to offer flexible fulfillment options that are connected to your inventory system.
    *   **Click-and-Collect**: This is a popular option for bakeries. You can configure a "Pick up in Store" shipping method in the **Website** app under **Configuration -> Shipping Methods**. When a customer selects this option at checkout, no shipping fee is applied, and a delivery order is created in your inventory system for internal tracking, so your staff knows to prepare the order for customer pickup.[5, 12]
    *   **Local Delivery**: For bakeries that offer home delivery, you can set up shipping methods with fixed or rule-based pricing (e.g., based on weight or order total). Odoo also has connectors for major shipping carriers like DHL and FedEx, which can calculate shipping rates in real-time and print shipping labels.[5] For food-specific delivery, Odoo can integrate with third-party delivery platforms like Uber Eats, DoorDash, and Zomato through connectors like UrbanPiper. This allows orders from these platforms to flow directly into your Odoo system, streamlining the entire online delivery process.[58, 59, 60]
