Chapter 4: From Opportunity to Engagement - The Sales & Quoting Process
=======================================================================

This chapter marks the beginning of the end-to-end "Lead-to-Cash" workflow configuration. [cite: 192] We will focus on the "Quote" portion of the process, detailing how to set up Odoo's Sales and CRM applications to manage the client acquisition and contracting phase. [cite: 193] The central and most critical element in this chapter is the Service Product. [cite: 194] Its correct configuration is the linchpin that connects the sales process with project delivery and financial accounting, enabling the seamless automation that is Odoo's hallmark for service businesses. [cite: 195]

Section 4.1: The Cornerstone: Configuring Service Products
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In Odoo, every line item on a sales order must be a "product." [cite: 196] For service businesses, these products are not physical goods but representations of the services offered. [cite: 197] The configuration of these service products acts as the "DNA" of a transaction, carrying all the necessary instructions for how a sale should be delivered, tracked, and, most importantly, billed. [cite: 198] An incorrectly configured service product will break the entire automated workflow, leading to manual workarounds and revenue leakage. [cite: 199]

To begin, navigate to Sales ‣ Products ‣ Products and click New. [cite: 200]

    * **Product Type:** The first and most fundamental setting is the Product Type, found in the General Information tab. [cite: 201] For any service, this must be set to Service. [cite: 202] This tells Odoo that the product does not have stock levels to manage. [cite: 202]

    * **Invoicing Policies:** This is the most critical setting for determining how and when a client will be billed. [cite: 203] Located in the General Information tab, this field dictates the entire invoicing workflow. [cite: 204] A service firm will typically use one of three main policies:
        * **Based on Timesheets (Time & Materials):** This is the most common policy for consulting and professional services. [cite: 205] The client is billed for the actual hours of work performed. [cite: 206] When this policy is selected, the invoice will be generated based on the hours logged in the Timesheets app for the associated project task. [cite: 207]
        * **Prepaid/Fixed Price:** This policy is used for services sold at a fixed price, such as a monthly retainer, a discovery workshop, or a fixed-scope project deliverable. [cite: 208] The full amount can be invoiced immediately upon confirmation of the sales order, regardless of the time spent. [cite: 209]
        * **Based on Milestones:** For large, long-term projects, this policy allows for progressive billing as specific, predefined milestones are completed. [cite: 210] An invoice can be created for each milestone as it is reached, ensuring a steady cash flow throughout the project's lifecycle. [cite: 211]

    * **Service Tracking (Create on Order):** This setting, located in the Sales tab of the product form, is the magic that automates the handoff from the sales team to the delivery team. [cite: 212] It tells Odoo what to do in the Project app when a sales order containing this product is confirmed. [cite: 213] The options are:
        * **Nothing:** No project or task is created automatically. [cite: 214] This is rarely used for billable services. [cite: 214]
        * **Create a task in an existing project:** This is useful for ongoing work or retainers for an existing client, where new tasks are added to a master client project. [cite: 215] A Project field will appear, requiring you to select the destination project. [cite: 216]
        * **Create a new project for the sales order:** This creates a brand-new project named after the sales order. [cite: 217] This is suitable when a single sales order represents a large, distinct project. [cite: 218]
        * **Create a project and task:** This is the most common and versatile setup. [cite: 219] It creates a new project and a new task within that project. [cite: 220] This is ideal for selling distinct service packages where each line item on the SO becomes a trackable task. [cite: 221]

**Configuration Example: "Consulting Hours" Product**

To illustrate, let's configure a standard time-and-materials consulting service: [cite: 222]

* Product Name: Consulting Services [cite: 222]
* Product Type: Service [cite: 222]
* Invoicing Policy: Based on Timesheets [cite: 222]
* Unit of Measure: Hours (ensure this is enabled in settings) [cite: 222]
* Navigate to the Sales tab. [cite: 222]
* Create on Order: Create a project and task [cite: 223]
* Sales Price: Enter the hourly billing rate (e.g., 150.00). [cite: 223]

.. figure:: /images/product_form_timesheet.png
   :alt: Configuring a service product for timesheet-based billing.
   :align: center
   :width: 80%

   *Fig 4.1: Detailed configuration of a service product for time-and-materials billing, highlighting the critical 'Invoicing Policy' and 'Create on Order' fields.* [cite: 225]

Section 4.2: Managing the Sales Funnel with CRM
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Odoo CRM app provides the tools to manage the sales process that precedes the quotation. [cite: 225] A well-structured CRM pipeline ensures that potential deals are tracked systematically from initial interest to a successful close. [cite: 226]

    * **Pipeline Configuration:** Navigate to CRM ‣ Configuration ‣ Stages. Here, you can define the stages of your sales process. [cite: 227] A typical pipeline for a consulting firm might look like:
        * New: Initial lead or inquiry. [cite: 228]
        * Qualification: The lead has been contacted, and a potential need is identified. [cite: 229]
        * Proposition: A formal proposal or quotation has been sent to the prospect. [cite: 230]
        * Negotiation: The terms of the proposal are being discussed. [cite: 231]
        * Won: The deal is closed, and the contract is signed. [cite: 231]
        * Lost: The opportunity will not be moving forward. [cite: 232]

    * **Lead Generation and Conversion:** Odoo provides multiple channels to capture leads, including manual creation, an automated email alias (where emails sent to sales@yourcompany.odoo.com create leads), and website contact forms. [cite: 232] Once a lead is deemed to have a genuine potential for business (e.g., after an initial discovery call), it should be converted into an Opportunity. [cite: 233] This action moves the record from a simple list of leads into your active sales pipeline, where it can be tracked through the stages defined above. [cite: 234]

Section 4.3: Building and Managing Quotations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once an opportunity reaches the "Proposition" stage, it's time to create a formal quotation. [cite: 235]

* **Creating Quotations from Opportunities:** Odoo provides a seamless link between the CRM and Sales apps. [cite: 236] From an opportunity form, clicking the New Quotation button will create a new quote, automatically linking the customer and other relevant information. [cite: 237] This maintains a clean data trail and ensures the sales team can see all related quotes directly from the opportunity record. [cite: 238]

* **Quotation Templates:** For standardized service offerings, Quotation Templates can be a massive time-saver. [cite: 239] Navigate to Sales ‣ Configuration ‣ Quotation Templates. Here, you can create templates that pre-populate product lines, terms and conditions, and even have an expiration date. [cite: 240] This ensures consistency and dramatically speeds up the process of sending common proposals. [cite: 241]

* **Online Confirmation and Payment:** A key feature for accelerating the sales cycle is the ability for customers to confirm orders electronically. [cite: 242] When sending a quotation by email, the customer receives a link to a web version of the quote. [cite: 243] From this Customer Portal, they can review the details and, if the features are enabled (Sales ‣ Configuration ‣ Settings), they can provide an Online Signature and even make an Online Payment (e.g., a deposit) to confirm the order. [cite: 244] This action automatically converts the quotation into a confirmed sales order in Odoo, triggering the project creation workflows without any manual intervention from the salesperson. [cite: 245] This automation removes friction and delay from the most critical point in the sales process. [cite: 246]

.. figure:: /images/quotation_customer_portal.png
   :alt: Customer view of an online quotation with options to sign and pay.
   :align: center
   :width: 80%

   *Fig 4.2: The customer portal view, which allows clients to digitally sign and pay for a quotation, turning it into a sales order instantly.* [cite: 248]

By meticulously configuring service products and leveraging the integrated workflow between CRM and Sales, a service business can establish a robust, efficient, and largely automated front-end for its entire operation. [cite: 248]
