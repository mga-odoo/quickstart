************************************************
Chapter 4: Managing Products and Raw Materials
************************************************

The product master is the central repository of information for everything a bakery buys, produces, and sells. A well-structured product catalog is the backbone of an effective ERP system, as this data is used by the Inventory, Purchase, Manufacturing, Sales, and POS applications. This chapter details how to create and configure raw materials, finished goods, and product variants.

Creating Raw Materials (Ingredients)
=========================================

First, create a product record for every ingredient used in the bakery, from bulk items like flour and sugar to specialty items like vanilla extract and chocolate chips.

Navigate to **Inventory -> Products -> Products** and click **Create**. When creating an ingredient, pay close attention to the following fields on the product form:
    *   **Product Name**: A clear, descriptive name (e.g., "All-Purpose Flour").
    *   **Product Type**: This must be set to **Storable Product**. This tells Odoo to track the inventory quantity for this item.[20]
    *   **Unit of Measure (UoM)**: This is the unit used for inventory and production (e.g., kg, g, L).
    *   **Purchase Unit of Measure**: This is the unit in which you buy the ingredient from your supplier. For example, you might purchase flour in a "25kg Bag" but use it in recipes in "grams". Odoo can handle the conversion automatically if the UoMs are configured in the same category.[21, 22]
    *   **Purchase Tab**: Under this tab, you can add a list of **Vendors**. By specifying the supplier and their price for the ingredient, you can streamline the purchasing process, as Odoo will automatically suggest this vendor when creating a purchase order.[23]

.. image:: /images/chapter4/raw_material_form.png
   :alt: Product form for a raw material like 'Flour', showing key fields.

Creating Finished Goods
============================

Next, create product records for all the items you sell to customers, such as croissants, sourdough loaves, and custom cakes. These are the products that will appear on your POS screen and in your online store.

When creating a finished good, the following configurations are essential:
    *   **Product Name**: The customer-facing name of the product (e.g., "Sourdough Loaf").
    *   **Product Type**: This should also be set to **Storable Product** if you produce items for stock. If an item is baked strictly to order, it could be set as a consumable, but storable is generally recommended for bakeries.
    *   **Routes**: In the **Inventory** tab, the **Routes** configuration determines the product's workflow. For a baked good, you should select both **Manufacture** and **Buy**. Selecting "Manufacture" tells Odoo that this product is created internally using a Bill of Materials. Selecting "Buy" tells Odoo that this product can be sold.[22]
    *   **Sales Price**: Set the retail price in the **General Information** tab.
    *   **Point of Sale Tab**: This tab contains settings specific to the POS. Ensure **Available in POS** is checked. If the item is sold by weight (e.g., a rustic loaf), check **To Weigh With Scale**.[24]

Configuring Product Categories
==================================

Product categories are a powerful organizational tool that impacts multiple areas of Odoo. Taking the time to create a logical category structure will improve efficiency and user experience across the system. Categories can be managed under **Inventory -> Configuration -> Product Categories**.

A well-designed category structure provides benefits in several key areas:
    *   **Point of Sale**: In the POS interface, products are grouped by their category. A logical structure (e.g., "Breads," "Pastries," "Cakes," "Drinks") allows cashiers to navigate the screen quickly and efficiently, speeding up the checkout process, which is especially important during peak hours.[5]
    *   **eCommerce**: On the online store, product categories are used to build the main navigation menu and filtering options. This helps customers easily find what they are looking for, improving the online shopping experience and increasing conversion rates.[25]
    *   **Reporting & Analytics**: Sales reports can be grouped by category, allowing you to easily identify which types of products are your best sellers.
    *   **Accounting**: Product categories can be linked to specific income and expense accounts, automating the financial posting of sales and inventory valuation.

Because of this multi-purpose functionality, establishing a clear and comprehensive category tree at the beginning of the implementation is a high-leverage activity that pays dividends in usability and reporting accuracy down the line.

Advanced: Setting Up Product Variants
==========================================

Many bakery products are not uniform; they come with options. A celebration cake, for instance, might be available in different sizes, flavors, and with various frosting choices. Instead of creating dozens of separate products (e.g., "8-inch Chocolate Cake," "8-inch Vanilla Cake," "10-inch Chocolate Cake"), Odoo's product variants feature allows you to manage all these combinations under a single product template.

The configuration process is as follows:
    1.  **Enable Variants**: First, you must enable the feature. Navigate to **Point of Sale -> Configuration -> Settings** and check the box for **Variants**.[24]
    2.  **Create Attributes**: Go to **Point of Sale -> Configuration -> Attributes**. Here, you will define the types of options available. For a cake, you might create an attribute called "Size" and another called "Flavor".[24]
    3.  **Define Attribute Values**: For each attribute, define the possible values. For the "Size" attribute, the values could be "8-inch," "10-inch," and "12-inch." For "Flavor," they could be "Chocolate," "Vanilla," and "Strawberry".[24]
    4.  **Assign Attributes to a Product**: Create a new product (e.g., "Celebration Cake"). In the **Attributes & Variants** tab, add the "Size" and "Flavor" attributes. After adding the attributes and their values, save the product template. Odoo will automatically generate all possible unique combinations as product variants.[24, 26]
    5.  **Configure Variant Pricing**: You can set a price uplift for specific attribute values. For example, the 10-inch cake might cost an additional $10, and the 12-inch might cost an additional $20 compared to the base price of the 8-inch cake. This is done by clicking the **Configure** button next to the attribute on the product form and entering the extra price for each value.[24, 26]

When this product is selected in the POS or on the eCommerce site, the user or customer will be prompted to choose from the available options, and the price will adjust automatically.

.. image:: /images/chapter4/product_variants_config.png
   :alt: Configuring attributes and variants for a cake product in Odoo.
