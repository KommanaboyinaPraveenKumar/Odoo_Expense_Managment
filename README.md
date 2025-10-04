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
| **Authentication & User Management** | [cite_start]Upon first login/signup, a new **Company** and **Admin User** are auto-created, with the company using the selected country's currency[cite: 10, 11]. |
| **Expense Submission** | [cite_start]Employees can submit claims including **Amount** (which can be in a currency different from the company's default), **Category**, **Description**, and **Date**[cite: 18, 19]. |
| **Multi-Level Approval** | [cite_start]Supports a sequence of approvers (e.g., Manager, Finance, Director)[cite: 24, 31]. [cite_start]The expense moves to the next approver only after the current one approves or rejects it[cite: 32]. |
| **Conditional Approvals** | [cite_start]Rules support **Percentage** (e.g., 60% of approvers approve) or **Specific Approver** (e.g., If CFO approves, the expense is auto-approved)[cite: 38, 39, 40]. [cite_start]Hybrid rules can combine both flows[cite: 41]. |
| **Expense History** | [cite_start]Employees can **view their own expense history** (Approved, Rejected) and check the approval status[cite: 20]. |

### 3. Roles and Permissions

| Role | Permissions |
| :--- | :--- |
| **Admin** | [cite_start]Auto-create company on signup, **manage users**, set roles, **configure approval rules**, view all expenses, and **override approvals**[cite: 44]. |
| **Manager** | [cite_start]**Approve/reject expenses** (amount visible in company's default currency), view team expenses, and escalate as per rules[cite: 44]. |
| **Employee** | [cite_start]**Submit expenses**, view their own expenses, and check approval status[cite: 44]. |

### 4. Technical Specifications & Integrations

#### Currency and Country Data
The application relies on external APIs for essential data:
* **Country and Currency Data:** Used for auto-setting the company's currency.
    * [cite_start]API Endpoint: `https://restcountries.com/v3.1/all?fields=name,currencies` [cite: 48]
* **Currency Conversions:** Required to convert submitted expense amounts to the company's base currency.
    * [cite_start]API Endpoint: `https://api.exchangerate-api.com/v4/latest/{BASE_CURRENCY}` [cite: 48]

#### Optional Features (OCR)
[cite_start]The system is designed to support **OCR for receipts**[cite: 46]. [cite_start]Employees can scan a receipt, and the OCR algorithm will auto-generate the expense with fields like amount, date, description, and expense type[cite: 47].

---
[cite_start]*Mockup provided at: [https://link.excalidraw.com/l/65VNwvy7c4X/4WSLZDTrhkA](https://link.excalidraw.com/l/65VNwvy7c4X/4WSLZDTrhkA)* [cite: 49]

