Chapter 7: Ensuring Client Success - Post-Delivery Support with Helpdesk
=============================================================================

The relationship with a client does not end when the final project invoice is paid. [cite: 342] Ongoing support, whether for bug fixes, user questions, or new requests, is a critical part of the service lifecycle. [cite: 343] Managing this post-delivery phase effectively is key to client retention and can also be a significant source of revenue. [cite: 344] The Odoo Helpdesk app provides a structured, professional system for managing all client support interactions. [cite: 345]

Section 7.1: Configuring Your Support Center
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Setting up a robust support center in Odoo begins with defining the structure through which tickets will be managed and resolved. [cite: 346]

    * **Helpdesk Teams:** The first step is to create one or more Helpdesk Teams. [cite: 347] This is done by navigating to Helpdesk ‣ Configuration ‣ Helpdesk Teams. [cite: 348] Teams can be organized based on function (e.g., Technical Support, Functional Support, Billing Inquiries), client tiers (e.g., Standard Support, Premium Support), or product lines. [cite: 349] Each team has its own dedicated email alias, pipeline, and set of members. [cite: 350]

    * **Ticket Pipeline (Stages):** For each team, you must configure a pipeline of Stages that represent the lifecycle of a support ticket. [cite: 351] These are fully customizable but a typical workflow might include stages such as: New, In Progress, Awaiting Customer, Solved, Canceled. [cite: 352] This Kanban-style view gives support managers an instant overview of the team's workload and the status of every ticket. [cite: 353]

    * **Ticket Creation Channels:** Odoo offers multiple channels for customers to submit support requests, ensuring accessibility and convenience. [cite: 354] These channels can be configured per team:
        * **Email Alias:** Each Helpdesk team can have a unique email address (e.g., support@yourcompany.odoo.com). [cite: 355] Any email sent to this address will automatically create a new ticket in that team's pipeline. [cite: 356]
        * **Website Form:** A customizable form can be embedded on the company website, allowing clients to submit structured support requests directly into Odoo. [cite: 357]
        * **Live Chat:** The Live Chat feature can be used to provide real-time support, and conversations can be converted into Helpdesk tickets with a single click if the issue requires further follow-up. [cite: 358]

Section 7.2: Defining Service Levels with SLA Policies
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A Service Level Agreement (SLA) defines the commitment of service you promise to your customers, such as the maximum time to resolve a critical issue. [cite: 359] Odoo's SLA Policies feature allows you to formalize these commitments and track your team's performance against them. [cite: 360]

    * **Creating SLA Policies:** Navigate to Helpdesk ‣ Configuration ‣ SLA Policies. [cite: 361] Here you can create rules that automatically apply to incoming tickets. [cite: 362] A policy is defined by a set of criteria:
        * **Helpdesk Team:** The policy applies only to tickets in a specific team. [cite: 363]
        * **Priority:** The policy can be triggered based on the ticket's priority (e.g., High, Medium, Low). [cite: 364]
        * **Ticket Type or Tags:** You can create policies for specific types of issues, such as "Bug Report" or "Billing Question." [cite: 365]

    * **Setting Performance Targets:** The core of an SLA policy is its target. [cite: 366] This defines what must be accomplished and by when. [cite: 367] For example, a policy could state that for any ticket with a "High" priority, the team must get it to the "In Progress" stage within 4 working hours of its creation. [cite: 367] Odoo will then calculate a deadline for each ticket that matches this policy, taking the team's configured working hours into account. [cite: 368] This deadline is clearly visible on the ticket, and the system will flag tickets that are approaching or have breached their SLA, providing a powerful tool for prioritizing work and managing customer expectations. [cite: 369]

.. figure:: /images/sla_policy_config.png
   :alt: Configuring an SLA Policy in Odoo Helpdesk.
   :align: center
   :width: 80%

   *Fig 7.1: The SLA Policy form, showing criteria such as Priority and the target to reach a specific stage within a set timeframe.* [cite: 371]

Section 7.3: The Integrated Support-to-Cash Workflow
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For many consulting firms, post-project support is not a free service but a billable one, often sold in pre-paid blocks of hours or on a time-and-materials basis. [cite: 371] Odoo's ability to integrate the Helpdesk app with Timesheets and Sales transforms the support desk from a pure cost center into a measurable and manageable revenue center. [cite: 372]

    * **Enabling Time Tracking on a Helpdesk Team:** To enable this workflow, you must activate time tracking for the relevant support team. [cite: 373]
        1.  Navigate to Helpdesk ‣ Configuration ‣ Helpdesk Teams and select the team to configure. [cite: 374]
        2.  On the team's settings page, scroll to the Track & Bill Time section. [cite: 375]
        3.  Check the boxes for Timesheets and Time Billing. [cite: 376]
        4.  When Timesheets is enabled, a Project field will appear. [cite: 376] You must select or create a project here. [cite: 377] This project will serve as the container for all timesheet entries logged against tickets in this team. [cite: 377] This is the critical link between Helpdesk and Project management. [cite: 378]

    * **The Complete Billing Workflow for Support:** Once configured, the process for billing support hours is seamless and mirrors the project billing workflow: [cite: 379]
        1.  A customer submits a ticket, which arrives in the configured Helpdesk team's pipeline. [cite: 379]
        2.  The support consultant works on the ticket. [cite: 380] They navigate to the Timesheets tab on the ticket form and log the time they spent resolving the issue (e.g., 2 hours). [cite: 380]
        3.  This timesheet entry needs to be linked to a billable sales order. [cite: 381] This can be done by selecting the appropriate Sales Order Item on the ticket form. [cite: 382] This could be a line item from a pre-sold "Support Pack" or a new time-and-materials sales order created for this specific request. [cite: 383]
        4.  The 2 hours logged on the ticket's timesheet are automatically added to the Delivered quantity on the linked sales order item. [cite: 384]
        5.  The accounting department can then navigate to that sales order and click Create Invoice to bill the client for the 2 hours of support work provided. [cite: 385]

This integrated flow provides full traceability from the initial customer request to the final payment. [cite: 386] It ensures that all billable support time is accurately captured and invoiced, preventing revenue leakage and providing clear data on the profitability of support contracts. [cite: 387]
