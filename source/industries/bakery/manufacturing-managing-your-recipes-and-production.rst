Chapter 7: Manufacturing: Managing Your Recipes and Production
**************************************************************

This chapter focuses on the heart of the bakery's operations: the transformation of raw ingredients into finished products. Odoo's Manufacturing application, also known as Material Requirements Planning (MRP), provides the tools to digitize recipes, manage production workflows, calculate costs accurately, and plan baking schedules efficiently.

7.1 Introduction to Odoo Manufacturing (MRP)
=============================================

Odoo's Manufacturing app is built around a few core concepts that work together to manage the production process [27, 34]:
    *   **Bill of Materials (BoM)**: This is the digital version of a recipe. It lists all the raw material components and the exact quantities needed to produce a specific finished product.
    *   **Work Centers**: These represent the different production stations in your bakery, such as a "Mixing Station," "Oven," or "Decorating Station."
    *   **Routings**: A routing defines the sequence of operations (steps) required to make a product, specifying which work center is used for each step and how long it should take.
    *   **Manufacturing Order (MO)**: This is the document that authorizes and tracks the production of a specific quantity of a product. It consumes the raw materials from the BoM and adds the finished goods to inventory.

7.2 Creating Recipes as Bills of Materials (BoMs)
===================================================

The first step in setting up manufacturing is to create a Bill of Materials for every product you bake. Navigate to **Manufacturing -> Products -> Bills of Materials** and click **Create**.

When creating a BoM, you will specify:
    *   **Product**: The finished good this BoM is for (e.g., "Sourdough Loaf").
    *   **Quantity**: The number of units of the finished product that this recipe yields (typically "1").
    *   **Components**: In the **Components** tab, you will add a line for each raw material (ingredient) required. For each component, you specify the product and the quantity needed to produce the yield defined above.[35, 36]

A well-defined BoM is the foundation for accurate inventory consumption and product costing. When you produce a Sourdough Loaf using this BoM, Odoo will automatically deduct the specified quantities of flour, water, salt, and starter from your inventory.

.. image:: /images/chapter7/bom_form.png
   :alt: The Bill of Materials form in Odoo for a Sourdough Loaf, showing components and quantities.

7.3 Managing BoMs for Products with Variants
============================================

Many bakery items, like cakes, are sold in different sizes or flavors. Instead of creating a separate BoM for every single variant, Odoo provides a more efficient method to manage this complexity within a single BoM.

This approach leverages the `Apply on Variants` field. Imagine a "Celebration Cake" product with a "Size" attribute (8", 10", 12"). The ingredients are the same, but the quantities change with the size.
    1.  Create one BoM for the main "Celebration Cake" product template.
    2.  In the **Components** tab, add the ingredient lines for the 8-inch version (e.g., 500g Flour). In the `Apply on Variants` column for these lines, select the "Size: 8-inch" variant.
    3.  Add another set of ingredient lines for the 10-inch version (e.g., 750g Flour). In the `Apply on Variants` column for these lines, select the "Size: 10-inch" variant.
    4.  Repeat for the 12-inch version.

Now, you have a single "super BoM" that contains the recipe for all variants. When you create a Manufacturing Order for a specific variant (e.g., a 10-inch cake), Odoo will intelligently pull only the component lines that are designated for that specific variant.[26] This method is far more efficient to maintain than managing dozens of separate BoMs; if an ingredient in the frosting recipe changes, you only need to update it in one place.

7.4 The Production Workflow
===========================

The daily production process is managed through Manufacturing Orders (MOs).
    1.  **Create MO**: To start production, go to **Manufacturing -> Operations -> Manufacturing Orders** and click **Create**. Select the product to be manufactured (e.g., "Croissant") and the quantity. Odoo will automatically load the corresponding BoM.
    2.  **Check Availability**: Odoo will show you if you have enough raw materials in stock to complete the order. If not, you can directly trigger a purchase order.
    3.  **Plan & Produce**: Once confirmed, the MO is ready for production. The bakers follow the steps outlined in the MO's Work Orders (e.g., mixing, proofing, baking). As they complete each step, they can track their progress in the system, either from a desktop or a tablet on the shop floor.
    4.  **Mark as Done**: When the baking is complete, clicking **Mark as Done** on the MO will trigger the inventory moves: Odoo consumes the raw materials from stock and adds the specified quantity of finished croissants to your on-hand inventory, making them available for sale.[37, 38]

7.5 Planning Production with the Master Production Schedule (MPS)
==================================================================

For bakeries with more complex scheduling needs, the Master Production Schedule (MPS) provides a high-level planning interface. Found under **Manufacturing -> Planning -> Master Production Schedule**, the MPS allows you to plan production over a period (days, weeks, or months). It considers forecasted demand from sales forecasts and actual demand from confirmed sales orders to help you decide what quantities of each product need to be baked and when. This helps in optimizing the use of critical resources like oven time and skilled bakers, ensuring you can meet demand without overproducing.[27, 39]
