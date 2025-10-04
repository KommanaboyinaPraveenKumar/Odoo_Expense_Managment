# Odoo_Expense_Managment


## 📝 README: Expense Management System

### Project Context

| Detail | Value |
| :--- | :--- |
| **Team Name** | **Code Coders** |
| **Team Members** | Praveen, Aadarsh, Likhitha, Surya|
| **Problem Statement** |Expense Management  |
| **Reviewer** | Aman Patel |

---

### 1. Overview

[cite_start]The Expense Management system is designed to streamline and automate the traditional, manual process of expense reimbursement, addressing common issues like long processing times, errors, and a lack of transparency[cite: 3]. The application supports a robust, multi-level approval workflow with flexible conditional rules, ensuring efficient and controlled expense processing.

### 2. Core Features

| Feature | Description |
| :--- | :--- |
| **Authentication & User Management** | Upon first login/signup, a new **Company** and **Admin User** are auto-created, with the company using the selected country's currency. |
| **Expense Submission** | Employees can submit claims including **Amount** (which can be in a currency different from the company's default), **Category**, **Description**, and **Date**. |
| **Multi-Level Approval** | [cite_start]Supports a sequence of approvers (e.g., Manager, Finance, Director). The expense moves to the next approver only after the current one approves or rejects it. |
| **Conditional Approvals** | [cite_start]Rules support **Percentage** (e.g., 60% of approvers approve) or **Specific Approver** (e.g., If CFO approves, the expense is auto-approved). Hybrid rules can combine both flows. |
| **Expense History** | Employees can **view their own expense history** (Approved, Rejected) and check the approval status. |

### 3. Roles and Permissions

| Role | Permissions |
| :--- | :--- |
| **Admin** | Auto-create company on signup, **manage users**, set roles, **configure approval rules**, view all expenses, and **override approvals**[. |
| **Manager** | **Approve/reject expenses** (amount visible in company's default currency), view team expenses, and escalate as per rules. |
| **Employee** | **Submit expenses**, view their own expenses, and check approval status. |

### 4. Technical Specifications & Integrations

#### Currency and Country Data
The application relies on external APIs for essential data:
* **Country and Currency Data:** Used for auto-setting the company's currency.
    * API Endpoint: `https://restcountries.com/v3.1/all?fields=name,currencies` 
* **Currency Conversions:** Required to convert submitted expense amounts to the company's base currency.
    * API Endpoint: `https://api.exchangerate-api.com/v4/latest/{BASE_CURRENCY}` 

#### Optional Features (OCR)
The system is designed to support **OCR for receipts**. Employees can scan a receipt, and the OCR algorithm will auto-generate the expense with fields like amount, date, description, and expense type.




