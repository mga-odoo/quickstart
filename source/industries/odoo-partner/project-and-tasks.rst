Chapter 5: Delivering Excellence - Project & Task Management
================================================================

With a contract signed and a sales order confirmed, the focus shifts from acquisition to delivery. [cite: 249] This chapter details the operational heart of a service business: managing the execution of projects and tasks using Odoo's Project and Timesheets applications. [cite: 250] The seamless, automated handoff from the sales process, configured in the previous chapter, is where the power of Odoo's integration first becomes truly tangible. [cite: 251]

Section 5.1: Automating the Handoff: From Sales Order to Project
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The manual transfer of information from a sales team to a project team is a common bottleneck in many service organizations, often leading to delays, miscommunication, and incomplete project setups. [cite: 252] Odoo eliminates this friction through the automated workflow configured on the service product. [cite: 253]

* **The Automated Workflow in Action:** When a sales order containing a service product (configured with a Create on Order policy) is confirmed, Odoo automatically executes the specified action in the Project app. [cite: 254] For example, if the product "Website Design Package" was set to "Create a project and task," confirming a sales order for this product will instantly:
    * Create a new Project. [cite: 255] By default, the project will be named after the sales order (e.g., "SO00123 - Smith Corp"), but this can be changed. [cite: 256]
    * Create a new Task within that project, named after the service product on the sales order line (e.g., "Website Design Package"). [cite: 257] The task will be automatically linked to the customer and the specific sales order item, ensuring full traceability from delivery back to the sale. [cite: 258]

* **Project Templates for Standardization:** For recurring types of projects, such as a standard "SEO Audit" or "New Client Onboarding," using Project Templates can further enhance automation and ensure consistency. [cite: 259] A project template can be pre-configured with a standard set of stages and even a list of common tasks that are required for that project type. [cite: 260] When configuring a service product, you can associate it with a specific project template. [cite: 261] Upon confirmation of the sales order, Odoo will create a new project that is a complete copy of the template, with all its predefined stages and tasks ready to go. [cite: 262] This practice is invaluable for standardizing service delivery and ensuring no critical steps are missed. [cite: 263]

.. figure:: /images/project_from_so.png
   :alt: The Project and Task smart buttons appearing on a confirmed Sales Order.
   :align: center
   :width: 80%

   *Fig 5.1: After confirming a sales order with a configured service product, smart buttons provide a direct link to the automatically created project and tasks.* [cite: 265]

Section 5.2: Managing Project Execution
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once a project and its tasks exist in the Project app, project managers and consultants have a central hub to manage the delivery process. [cite: 265]

    * **The Kanban View:** The default view for a project is a Kanban board, which provides a highly visual way to track task progress. [cite: 266] Each column represents a Stage in the workflow. [cite: 267] Project managers can easily configure these stages to match their delivery process (e.g., Backlog, To Do, In Progress, Client Review, Done). [cite: 267] Team members can then move tasks from one stage to the next via a simple drag-and-drop interface, providing an at-a-glance overview of the project's status. [cite: 268]

    * **Advanced Views for Deeper Planning:** Beyond the Kanban view, the Project app offers other powerful visualization tools:
        * **Gantt View:** Essential for planning project timelines. [cite: 269] It displays tasks on a horizontal time chart, allowing project managers to visualize task durations, set deadlines, and create dependencies between tasks (e.g., Task B cannot start until Task A is complete). [cite: 270]
        * **Calendar View:** Provides a standard calendar interface, useful for scheduling tasks and meetings with specific deadlines. [cite: 271]
        * **Map View:** For field service businesses, this view plots tasks on a map based on the customer's address, helping to plan efficient travel routes for on-site appointments. [cite: 272]

    * **Collaboration and Documentation:** Each task in Odoo serves as a mini-collaboration hub. [cite: 273] The chatter at the bottom of the task form logs all changes, allows team members to post messages, and can be used to attach relevant documents (e.g., design mockups, client feedback). [cite: 274] This keeps all communication and documentation related to a specific piece of work in one easily accessible place. [cite: 275]

Section 5.3: The Lifeblood of Billing: Tracking Time and Expenses
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For any service business billing on a time-and-materials basis, accurate and consistent time tracking is the lifeblood of its revenue stream. [cite: 276] The Timesheets app in Odoo is fully integrated with Project, making this process straightforward for consultants and transparent for managers. [cite: 277]

    * **Recording Timesheets:** Employees can record their billable hours in several ways, ensuring flexibility and ease of use:
        * **Directly on the Task:** This is the most common method. [cite: 278] Open the specific task in the Project app, navigate to the Timesheets tab, and click Add a line. [cite: 279] The employee selects the date, provides a description of the work performed, and enters the duration in hours. [cite: 280]
        * **Using the Timesheets App:** The dedicated Timesheets app provides a weekly or monthly grid view where employees can quickly enter time against different projects and tasks. [cite: 281]
        * **With the Task Timer:** On the task form, a Start button acts as a timer. [cite: 282] Clicking it starts a real-time clock, and clicking Stop automatically creates a timesheet entry for the elapsed duration. [cite: 283]

    .. figure:: /images/task_timesheet_entry.png
        :alt: Adding a timesheet line to a project task.
        :align: center
        :width: 80%

    *Fig 5.2: The Timesheets tab on a project task, where consultants log their billable hours with descriptions of the work performed.* [cite: 285]

    * **Submitting and Approving Expenses:** Project work often involves costs beyond just time, such as travel, software licenses, or materials. [cite: 285] The Expenses app allows employees to capture these costs and link them directly to the project for accurate profitability tracking and client re-invoicing. [cite: 286] An employee creates a new expense in the Expenses app, filling in the description, amount, and attaching a receipt. [cite: 287] Crucially, they select the correct Analytic Distribution, which links the expense to the specific project's financial account. [cite: 288] If the expense is to be billed back to the client, they also select the corresponding Sales Order in the "Customer to Reinvoice" field. [cite: 289] The expense is then submitted for approval by a manager. [cite: 290] Once approved and posted, it becomes available for invoicing on the sales order. [cite: 291]

This disciplined tracking of all time and expenses within Odoo ensures that no billable work is lost and provides the raw data needed for the accurate invoicing and profitability analysis covered in the subsequent chapters. [cite: 292]
