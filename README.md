# 🛒 E-Commerce Inventory & Customer Retention Tracking

![SQL](https://img.shields.io/badge/SQL-Advanced-blue) ![DBMS](https://img.shields.io/badge/DBMS-3NF%20Normalized-purple) ![Status](https://img.shields.io/badge/Status-Complete-green)

## Overview
A fully normalized relational database system for managing e-commerce inventory, automating stock alerts, and analysing customer retention patterns. Demonstrates core DBMS design principles applied to a real-world business scenario.

---

## Problem Statement
E-commerce platforms face two critical data challenges:
- Inventory running out silently (lost sales)
- Customers churning without early warning signals

This project addresses both through schema design, SQL triggers, and analytical queries.

---

## Database Schema

| Table | Description |
|-------|-------------|
| `Users` | Customer profiles and signup dates |
| `Products` | Inventory counts, prices, and categories |
| `Orders` | Order dates, total amounts, shipping status |
| `Order_Items` | Bridge table linking Orders ↔ Products (many-to-many) |

> The schema satisfies **Third Normal Form (3NF)** — no data redundancy, full referential integrity.

---

## Key Features

### 1. 3NF Database Design
Designed schema from scratch ensuring 3rd Normal Form compliance — eliminating data redundancy and enforcing referential integrity via foreign key constraints.

### 2. Automated Inventory Alerts (Triggers)
SQL Triggers automatically update product status to `Low Stock` or `Out of Stock` when order fulfillment reduces inventory below defined thresholds — no manual monitoring needed.

### 3. Customer Retention Analytics
Used `COUNT`, `SUM`, `GROUP BY`, and `HAVING` to identify:
- 🌟 **VIP Customers** — total spend > $500
- 🔁 **Churned Customers** — no orders in the last 90 days

---

## SQL Concepts Used
`3NF Normalization` · `Triggers` · `Joins` · `Subqueries` · `Aggregate Functions (COUNT, SUM)` · `GROUP BY / HAVING` · `Foreign Keys` · `Bridge Tables`

---

## Business Impact
- Prevents stock-outs through real-time automated alerts
- Enables data-driven retention strategy by identifying at-risk customers early
- Provides a production-ready schema pattern applicable to any e-commerce platform

---

## Author
**Nahida Banoo** — BSc (Hons) Computer Science, University of Delhi  
Research: Financial Fraud Detection (Conference Paper, 2024)
