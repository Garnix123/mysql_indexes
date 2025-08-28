# ⚡ SQL Indexing & Query Optimization – Lucky Shrub

## 🚀 Project Overview
This mini-project shows how small SQL changes can deliver **big performance wins** for the Lucky Shrub dataset. We:
- **Select only needed columns** instead of `SELECT *`.
- **Add a targeted index** to accelerate client lookups.
- **Refactor a non-sargable search** (`LIKE '%Tolo'`) into an index-friendly search using a derived, indexed column.  
These techniques cut unnecessary I/O, reduce latency, and make queries scale as data grows. :contentReference[oaicite:0]{index=0}

---

## 🧱 Schema & Seed Data (excerpt)
Two tables are used:
- `Orders(OrderID, ClientID, ProductID, Quantity, Cost, Date)` with sample rows across 2020–2022.
- `Employees(EmployeeID, FullName, Role, Department)`.  
Both are created and populated in the script. :contentReference[oaicite:1]{index=1}

---

## 🎯 What Problem Did I Solve?
1) **Over-fetching columns** → wastes bandwidth and CPU.  
2) **Slow client lookups** on `Orders` when filtering by `ClientID`.  
3) **Unindexable name search** (`LIKE '%Tolo'`) on `Employees`, forcing full scans.  
The solution applies column pruning, proper indexing, and query rewrites to enable index usage. :contentReference[oaicite:2]{index=2}

---
