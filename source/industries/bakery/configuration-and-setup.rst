Chapter 3: Initial System Setup
*******************************

Before diving into specific business workflows, a set of foundational configurations must be completed. This chapter covers the initial steps of installing the necessary applications, setting up core company information, and establishing user access controls. These steps create the essential framework upon which the entire bakery management system will be built.

3.1 Installing the Essential Bakery Apps
=========================================

The first practical step in any Odoo implementation is to install the required applications. Odoo's modularity means you only install what you need, keeping the system lean and focused. For a typical bakery that handles in-store sales, wholesale orders, online presence, and in-house production, the following suite of apps is recommended as a starting point.[5, 12]

To install apps, navigate to the main **Apps** menu from the Odoo dashboard. Use the search bar to find and install each of the following:
    *   Point of Sale
    *   Sales
    *   Purchase
    *   Inventory
    *   Manufacturing
    *   Invoicing
    *   Accounting
    *   Website
    *   eCommerce

.. image:: /images/chapter3/app_dashboard.png
   :alt: Odoo Apps Dashboard showing essential bakery apps installed.

Each app provides a specific set of functionalities, and their true power is realized through their seamless integration. For example, a sale in the Point of Sale app will automatically trigger actions in Inventory, Invoicing, and Accounting.

3.2 Configuring Company Information
===================================

Once the applications are installed, the next step is to configure the bakery's master data. This information will be used across the system on documents such as quotations, purchase orders, and invoices.

Navigate to **Settings -> General Settings**. Under the **Companies** section, click on **Update Info**. Here, you will configure:
    *   **Company Details**: The legal name, address, phone number, email, and website of the bakery.
    *   **General Information**: Set the company's currency (e.g., USD, EUR). This will be the default currency for all financial transactions.
    *   **Tax Information**: Enter the company's tax ID (e.g., VAT number, EIN). This is crucial for tax calculation and reporting.[17]

Next, it is essential to configure the fiscal periods for accounting. Navigate to the **Accounting** app and go to **Configuration -> Settings**. Here, you can define the **Fiscal Year**, which typically aligns with the calendar year but can be adjusted based on the bakery's financial reporting schedule. This is also where you would later import opening balances to establish the starting financial position of the company in Odoo.[18]

3.3 Setting Up Users, Roles, and Access Rights
================================================

Proper user management is fundamental to both security and system usability. You should create a user account for every employee who will interact with Odoo. However, not every user needs access to all information. A baker, for example, does not need to view sensitive financial reports, and a cashier primarily needs access to the POS interface.[19]

Configuring access rights correctly serves two purposes. First, it secures sensitive data. Second, and equally important, it simplifies the user experience. By limiting the menus and options a user can see, you present them with a cleaner, more focused interface tailored to their specific job role. This reduces confusion, minimizes the risk of errors, and significantly improves user adoption—a key factor for a successful project.[11, 14]

The process involves these steps:
    1. **Create Users**: Navigate to **Settings -> Users & Companies -> Users**. Click **Create** to add a new user, providing their name and email address.
    2. **Assign Application Access**: On the user form, you will see a matrix of installed applications. You can grant access to specific applications based on the user's role. For example:
        * **Cashier**: Should only have access to "Point of Sale (User)".
        * **Baker/Production Manager**: Needs access to "Manufacturing (User)" and "Inventory (User)".
        * **Manager/Owner**: Will likely need broader access, such as "Sales (Administrator)", "Accounting (Accountant)", and full access to other key apps.

For more granular control, Odoo uses **User Groups**. Each application comes with pre-configured groups (e.g., "User" and "Administrator"). Assigning a user to the "User: Show Full Accounting Features" group, for instance, grants them more capabilities within the Accounting app than a user assigned only to "Billing". This system allows for precise control over what each user can see and do within the platform.
