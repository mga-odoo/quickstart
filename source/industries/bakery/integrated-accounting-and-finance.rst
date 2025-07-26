Chapter 11: Integrated Accounting and Finance
*********************************************

The ultimate benefit of an integrated ERP system is a single, real-time view of your company's financial health. Because Odoo's **Accounting** application is connected to all operational apps (Sales, POS, Purchase, Inventory), most financial transactions are recorded automatically, drastically reducing manual bookkeeping efforts and providing accurate financial data.

11.1 Customer Invoicing and Payments
=====================================

Every sale, whether through the POS, a wholesale Sales Order, or an eCommerce order, generates the necessary financial entries. The workflow includes:
    *   **Invoice Creation**: Invoices are created automatically from confirmed sales orders or can be generated from POS sessions.
    *   **Payment Registration**: When a customer pays an invoice (either at the POS, online, or via a bank transfer for a wholesale order), the payment is registered in Odoo and reconciled against the corresponding invoice.
    *   **Follow-up**: Odoo can automatically send payment reminders for overdue wholesale invoices, improving cash flow.[18]

11.2 Managing Vendor Bills and Expenses
========================================

The accounts payable process is also streamlined:
    *   **Vendor Bills**: As described in Chapter 5, vendor bills are created from purchase orders and validated in the Accounting app. You can set up payment schedules and process batch payments to suppliers.
    *   **Employee Expenses**: If employees incur costs on behalf of the bakery (e.g., a delivery driver purchasing fuel), they can submit an expense report through the **Expenses** app. Once approved, this creates the necessary journal entries for reimbursement and cost tracking.[61]

11.3 Bank Reconciliation
========================

To ensure your books are always accurate, Odoo's bank reconciliation feature is essential. You can configure a direct link to your bakery's bank account, which will automatically import bank statement lines into Odoo every day.

The reconciliation process, found in the **Accounting** dashboard, presents a simple interface where you can match imported bank transactions (e.g., an incoming payment from a wholesale client) against open invoices in Odoo. For recurring transactions like bank fees, you can create reconciliation models to automate the matching process. This keeps your financial records perfectly aligned with your bank statements with minimal manual effort.[18, 62]
