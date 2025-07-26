Chapter 6: Monetizing Your Services - Invoicing & Revenue Recognition
===========================================================================

This chapter closes the loop on the primary "Quote-to-Cash" process. [cite: 293] It focuses on how to leverage the data meticulously captured during project execution—the timesheets and expenses—to generate accurate, timely invoices. [cite: 294] This is where the service firm monetizes its efforts and recognizes revenue. [cite: 295] Odoo's integrated nature ensures that the invoicing process is not a separate, manual task but a direct and logical continuation of the work already performed. [cite: 296]

Section 6.1: Invoicing Based on Time & Materials
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This is the most dynamic invoicing model for service businesses, directly linking the work performed to the amount billed. [cite: 297] The setup completed in previous chapters makes this process remarkably efficient. [cite: 298]

    * **The Automated Data Flow:** As consultants log their hours in the Timesheets app against a specific task, Odoo performs a critical background action. [cite: 299] The hours recorded automatically update the Delivered quantity on the corresponding line item of the original sales order. [cite: 300] For example, if the sales order was for 20 hours of "Consulting Services" and a consultant logs 8 hours, the Delivered quantity on the SO will change to 8. [cite: 301] This provides real-time visibility of billable work directly on the sales document. [cite: 301]

    * **Creating the Invoice:** When it's time to bill the client (e.g., at the end of the week or month), the process is straightforward: [cite: 302]
        1.  Navigate to the original Sales Order. [cite: 302]
        2.  Observe that the Delivered column reflects the total hours logged and ready for invoicing. [cite: 303]
        3.  Click the Create Invoice button in the top-left corner. [cite: 304]
        4.  A pop-up window will appear. [cite: 304] Select Regular Invoice and click Create Draft Invoice. [cite: 305]
        5.  Odoo generates a draft customer invoice. [cite: 305] The invoice line will be for the quantity of hours in the "Delivered" field, not the originally ordered quantity. [cite: 306] This ensures you are billing only for the work that has actually been completed. [cite: 307]
        6.  The draft invoice can be reviewed, confirmed, and sent to the customer for payment. [cite: 308]

This workflow eliminates the need for accountants to manually collect timesheet reports and re-enter data, drastically reducing administrative overhead and the risk of billing errors. [cite: 309]

Section 6.2: Invoicing Based on Project Milestones
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For large-scale projects, billing is often tied to the completion of specific deliverables or phases, known as milestones. [cite: 310] This approach provides predictable cash flow for the service firm and allows the client to pay in installments as they see tangible progress. [cite: 311]

    * **Reaching and Confirming a Milestone:** The project manager is responsible for tracking the progress of the project against the predefined milestones. [cite: 312] When all the work associated with a particular milestone is complete, it must be marked as "Reached." [cite: 313] This is done on the sales order by navigating to the Milestones smart button and checking the box in the Reached column for the completed milestone. [cite: 314]

    * **Invoicing the Reached Milestone:** Once a milestone is marked as reached, it becomes available for invoicing. [cite: 315]
        1.  Return to the Sales Order. [cite: 316]
        2.  Click Create Invoice. [cite: 316]
        3.  Select Regular Invoice and create the draft. [cite: 316]
        4.  Odoo will intelligently create a draft invoice that only includes the line item(s) for the milestone(s) that have been marked as reached. [cite: 317] Milestones that are still in progress will not be included. [cite: 318]

This allows the firm to issue multiple, partial invoices against a single sales order over the project's lifetime, perfectly aligning billing with project delivery. [cite: 319]

Section 6.3: Re-invoicing Expenses and Purchases
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Project-related costs, such as travel, accommodation, or specific materials purchased for the client, are often re-billed. [cite: 320] The key to automating this is the Analytic Distribution set when the expense or purchase was recorded. [cite: 321]

    * **The Automated Flow:** When an employee expense or a vendor bill is approved and posted with an analytic distribution linked to a sales order, Odoo automatically adds a new line item to that sales order. [cite: 322] The product on this new line is determined by the expense category's configuration. [cite: 323] For example, a "Hotel Stay" expense can be configured to create a "Travel Expenses" line on the sales order. [cite: 324] The cost from the original expense/bill becomes the basis for the sales price on this new line, which can be marked up if desired. [cite: 325]

    * **Invoicing the Expense:** This new line item now appears on the sales order with a delivered quantity of 1. [cite: 326] It can be invoiced along with the next batch of timesheets or as a separate invoice, simply by following the standard "Create Invoice" process. [cite: 326]

Section 6.4: Managing Recurring Revenue with Subscriptions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Many service firms have moved beyond one-off projects to more stable, recurring revenue models, such as monthly support retainers, managed service contracts, or Software-as-a-Service (SaaS) offerings. [cite: 327] The Odoo Subscriptions app is designed specifically to manage this business model. [cite: 328]

    * **The Use Case:** The Subscriptions app automates the entire lifecycle of a recurring service, from initial sale to ongoing billing and renewal management. [cite: 329] This is ideal for any service that requires regular, periodic invoicing without manual intervention each time. [cite: 330]

    * **Configuration:** The setup involves two key components:
        1.  **Recurring Plans:** Navigate to Subscriptions ‣ Configuration ‣ Recurring Plans. [cite: 331] Here, you define the billing cycles (e.g., "Monthly," "Quarterly," "Annually"). [cite: 332] Each plan specifies the billing frequency and duration. [cite: 332]
        2.  **Subscription Products:** Create a new product (or modify an existing one) in the Sales app. [cite: 333] On the product form, ensure the Subscription checkbox is ticked. [cite: 334] This designates it as a subscription product. [cite: 334] You can then link this product to one of the recurring plans you created. [cite: 335]

    * **The Automated Workflow:**
        1.  A salesperson sells the "Monthly Support Retainer" subscription product on a sales order. [cite: 336]
        2.  When the sales order is confirmed, Odoo automatically creates a Subscription record in the Subscriptions app. [cite: 337]
        3.  This subscription record will then automatically generate a new invoice for the client at the start of each billing period (e.g., on the 1st of every month) according to the rules of the assigned recurring plan. [cite: 338]

    * **Customer Portal and Self-Service:** A significant benefit of the Subscriptions app is its integration with the customer portal. [cite: 339] Clients can be given the ability to log in and manage their own subscriptions, view past invoices, update their payment methods, and even upgrade, downgrade, or cancel their plans (depending on the configured self-service options). [cite: 340] This empowers the customer and dramatically reduces the administrative burden on the service firm's staff. [cite: 341]
