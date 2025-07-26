
Chapter 3: Laying the Foundation - Initial Odoo Configuration
==============================================================

With the strategic and analytical groundwork complete, the process transitions to hands-on system configuration. [cite: 141] This chapter covers the foundational settings that must be established in Odoo before any business-specific workflows can be built. [cite: 142] These initial steps ensure the system has the correct company context, user permissions, and application suite to support the service business model. [cite: 143]

Section 3.1: System & Company Setup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This section details the configuration of the core system and company parameters. [cite: 144] These settings provide the legal and financial context for all subsequent transactions within Odoo. [cite: 145]

    * **Database Creation:** The very first step is the creation of the Odoo database. [cite: 146] The choice of hosting environment—Odoo Online (SaaS), Odoo.sh (PaaS), or an On-Premise server—should have been made during the initial planning phase based on the client's technical capabilities, customization needs, and budget. [cite: 147] Each has its own process for database creation. [cite: 148]

    * **Company Information:** Once the database is active, the primary task is to configure the company's details. [cite: 148]
        1.  Navigate to the Settings app. [cite: 149]
        2.  In the top-left corner, click on Users & Companies and select Companies. [cite: 149]
        3.  Select the default "My Company" record to edit it. [cite: 150]
        4.  Fill in all the essential information: Company Name, Address, Phone, Email, Website, and Tax ID (e.g., VAT, EIN). [cite: 150] This information will be used on all official documents, such as quotations, sales orders, and invoices. [cite: 151]
        5.  Set the company's default Currency. [cite: 152] This is a critical step that cannot be easily changed after transactions have been recorded. [cite: 152]

        .. figure:: /images/company_configuration.png
        :alt: Configuring the main company information in Odoo Settings.

        *Configuring the main company information in Odoo Settings.* [cite: 153]

    * **Fiscal Years & Chart of Accounts:** Proper financial setup is non-negotiable. [cite: 154]
        1.  Navigate to the Accounting app, then go to Configuration ‣ Settings. [cite: 155]
        2.  Under the Fiscal Periods section, ensure the Fiscal Year dates are correctly set. [cite: 156] Odoo will automatically propose a fiscal year ending on December 31st, but this can be adjusted. [cite: 157]
        3.  The most critical step is installing the correct Chart of Accounts (CoA). [cite: 158] Odoo provides pre-configured, country-specific CoA packages. [cite: 158]
        4.  In the Accounting settings, find the Fiscal Localization section and install the package that corresponds to the company's country. [cite: 159] This will install the standard accounts, taxes, and fiscal positions required for local compliance. [cite: 160] Attempting to build a CoA from scratch is highly discouraged and can lead to significant reporting and compliance issues. [cite: 161]

Section 3.2: User & Access Management
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A secure and efficient ERP system relies on a well-defined access control structure. [cite: 162] Odoo's user management allows for granular control over what each user can see and do. [cite: 163] The guiding principle should be that of least privilege: users should only have access to the information and actions necessary to perform their job functions. [cite: 164]

* **Creating Users:**
    1.  Navigate to Settings ‣ Users & Companies ‣ Users. [cite: 165]
    2.  Click New to create a user. [cite: 165]
    3.  Enter the user's Name and Email Address. [cite: 166] The email address will be their login and is used for system notifications. [cite: 166]
    4.  New users are sent an invitation email to set their password and log in for the first time. [cite: 167]

* **Configuring Access Rights:** Odoo's security model is based on User Groups. [cite: 168] Each application (e.g., Sales, Project, Accounting) comes with several pre-configured groups that correspond to different levels of access, such as "User" or "Administrator." [cite: 169] When editing a user, you will see a section for each installed application. [cite: 170] Within each application section, you can assign the user to a specific group from a drop-down menu. [cite: 171] For example, for the Sales application, the options are typically "User: Own Documents Only," "User: All Documents," and "Administrator." [cite: 172] Assigning a user to a group grants them all the permissions associated with that group. [cite: 173] This includes visibility of menus, access to records (read, write, create, delete), and the ability to perform certain actions. [cite: 174]

* **Role-Based Permission Setup:** For a service business, it is best practice to define standard roles and assign a consistent set of permissions. [cite: 175] This ensures uniformity and simplifies onboarding new employees. [cite: 176]

.. list-table:: Role-Based Permission Setup
   :widths: 20 20 25 35
   :header-rows: 1

   * - Role
     - Application
     - Access Level
     - Rationale
   * - Consultant/Employee
     - Project
     - User
     - Can see and update their assigned tasks. [cite: 176]
   * -
     - Timesheets
     - User
     - Can log their own timesheets. [cite: 176]
   * -
     - Expenses
     - User
     - Can submit their own expenses for reimbursement. [cite: 176]
   * - Project Manager
     - Project
     - Administrator
     - Can create new projects, manage all tasks, and see reporting. [cite: 176]
   * -
     - Sales
     - User: All Documents
     - Can view sales orders to understand project scope and create invoices. [cite: 176]
   * -
     - Accounting
     - Billing
     - Can create and manage customer invoices and vendor bills. [cite: 176]
   * - Salesperson
     - CRM
     - User
     - Manages their own leads and opportunities in the pipeline. [cite: 176]
   * -
     - Sales
     - User: All Documents
     - Can create and manage quotations and sales orders. [cite: 176]
   * - Accountant
     - Accounting
     - Accountant
     - Full access to all accounting functions, including chart of accounts, journal entries, and financial reports. [cite: 176]
   * - System Administrator
     - Settings
     - Administrator
     - Has access to all system settings, including user creation and app installation. [cite: 176]

Section 3.3: Installing Core Applications
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

With the foundational settings in place, the next step is to install the suite of Odoo applications that will power the service business's end-to-end workflow. [cite: 177] While Odoo offers hundreds of apps, a focused selection is key to a lean and effective implementation. [cite: 178]

Navigate to the Apps module from the main Odoo dashboard. [cite: 179] Use the search bar to find and install the following essential applications. [cite: 180] Installing a primary app often installs its dependencies automatically (e.g., installing Sales also installs Invoicing). [cite: 181]

    * **CRM:** For managing the sales pipeline, from lead generation to opportunity qualification. [cite: 182]
    * **Sales:** The core application for creating quotations and sales orders, which will serve as the trigger for project creation. [cite: 183]
    * **Project:** The central hub for service delivery, where all projects and tasks will be managed. [cite: 184]
    * **Timesheets:** Essential for tracking the time employees spend on project tasks, which is the basis for billing in a time-and-materials model. [cite: 185]
    * **Invoicing / Accounting:** While Invoicing is often sufficient for billing, installing the full Accounting app provides comprehensive financial management, including the chart of accounts, bank reconciliation, and financial reporting. [cite: 186] For any serious business, the full Accounting app is a necessity. [cite: 187]
    * **Expenses:** Allows employees to submit and get reimbursed for project-related expenses, which can then be re-invoiced to the client. [cite: 188]
    * **Subscriptions:** Crucial for any service firm that offers retainers, support contracts, or any other form of recurring service. [cite: 189] This app automates recurring billing and revenue management. [cite: 190]
    * **Helpdesk:** For managing post-project support, client inquiries, and bug reports in a structured ticketing system. [cite: 190]

By completing these foundational steps, the Odoo system is now prepared for the detailed configuration of the business-specific workflows that will be covered in the subsequent chapters. [cite: 191]
