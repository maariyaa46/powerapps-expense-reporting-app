# 💼 Power Apps – Expense Reporting Canvas App

This repository contains the exported files and documentation for a low-code **Expense Reporting App** built using Microsoft Power Apps (Canvas App). It helps users record, track, and manage business expenses and related line items using **Dataverse tables** for secure storage and future scalability.

---

## 🚀 Overview

The app enables:
- Submitting new expense entries
- Adding detailed line items under each expense
- Linking expenses to cost centers with assigned approver emails
- Storing data securely in Microsoft Dataverse

It’s ideal for internal teams who need a structured and low-code solution for expense reporting.

---

## 🧭 How the App Works

### 🖥️ User Interface Layout
The app is structured into two primary sections:
- **Left Panel (Gallery)**: Displays a list of records (expenses or line items)
- **Right Panel (Form)**: Allows users to add or edit selected records

This layout makes it intuitive to view and manage data simultaneously.

---

### 1. **Expense Entry Screen**
- **Left (Gallery)**: Shows a list of submitted expenses
- **Right (Form)**: Form fields include:
  - `Expense Name`
  - `Price`
  - `Quantity`
  - `Cost Center` (lookup)
- **Calculated Total** = `Price × Quantity`
- Data is saved to the `Expense` table in Dataverse
- Lookup fetches the approver email based on the selected cost center

---

### 2. **Line Items Screen**
- **Left (Gallery)**: Shows line items linked to a selected expense
- **Right (Form)**: Input fields for:
  - `Description` (e.g., Travel, Hotel)
  - `Amount`
- Line items are saved to the `Line Items` table and linked to the relevant expense

---

### 3. **Cost Center Table**
- Managed separately (usually by an admin)
- Fields:
  - `Center Name`
  - `Approver Email` (used for future approvals in Power Automate)

---

