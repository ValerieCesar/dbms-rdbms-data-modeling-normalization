# Database Normalization

## 🧾 What is Normalization?

**Normalization** is a systematic approach in database design that organizes data to reduce redundancy and improve data integrity. It involves dividing large tables into smaller, related tables and defining relationships among them.

---

## 🎯 Goals of Normalization
- Eliminate redundant data (e.g., storing the same data in more than one table)
- Ensure logical data dependencies
- Improve data consistency and integrity
- Optimize storage and update efficiency

---

## 📐 Normal Forms

Normalization is performed in steps called **Normal Forms**. Each form builds upon the previous one.

---

### 🔹 First Normal Form (1NF)
- Eliminate repeating groups
- Ensure each field contains only **atomic** (indivisible) values
- All entries in a column must be of the same type

✅ Example:  
Convert a table storing multiple phone numbers in one column into separate rows or columns.

---

### 🔹 Second Normal Form (2NF)
- Must first be in 1NF
- Eliminate **partial dependencies** — when a non-key attribute depends only on part of a composite key

✅ Example:  
Split a table into `Students` and `Courses` if course data only partially depends on student-course composite key.

---

### 🔹 Third Normal Form (3NF)
- Must first be in 2NF
- Eliminate **transitive dependencies** — when non-key attributes depend on other non-key attributes

✅ Example:  
Move department descriptions from the `Employee` table into a separate `Departments` table.

---

## 🧱 Normalization Summary Table

| Normal Form | Key Rule                                    | Goal                                  |
|-------------|---------------------------------------------|----------------------------------------|
| 1NF         | Atomic values, no repeating groups          | Structure data into tables             |
| 2NF         | No partial dependencies                     | Remove partial dependencies            |
| 3NF         | No transitive dependencies                  | Ensure only key-based dependencies     |

---

## ⚠️ Data Redundancy Example (Before Normalization)

| Employee_ID | Name   | Dept   | Dept_Location |
|-------------|--------|--------|----------------|
| 101         | Alice  | HR     | New York       |
| 102         | Bob    | HR     | New York       |

✅ Department info is repeated!

---

## ✅ After Normalization (Split Tables)

**Employees Table**

| Employee_ID | Name   | Dept_ID |
|-------------|--------|---------|
| 101         | Alice  | 1       |
| 102         | Bob    | 1       |

**Departments Table**

| Dept_ID | Dept   | Dept_Location |
|---------|--------|----------------|
| 1       | HR     | New York       |

---

## 🧠 Summary

- Normalize to reduce duplication and ensure data accuracy.
- Always begin with 1NF and progress step-by-step.
- Use keys and relationships to maintain logical structure.


![Image](https://github.com/user-attachments/assets/867afed8-288c-48d5-b0aa-f1c9f2ad2451)
