# ACID Properties of Database Transactions

## 🧾 What is ACID?

**ACID** is an acronym used to describe a set of properties that guarantee reliable processing of database transactions.

These properties ensure data integrity even in the case of power failures, crashes, or errors.

---

## 🔹 A – Atomicity

Atomicity ensures that all operations within a transaction are completed successfully. If one part fails, the entire transaction is rolled back.

✅ Example: If you transfer money from Account A to Account B, both debit and credit must succeed — or neither.

---

## 🔹 C – Consistency

Consistency ensures that a transaction brings the database from one valid state to another, maintaining all defined rules and constraints.

✅ Example: A transaction should not violate referential integrity, like inserting an order that references a non-existing customer.

---

## 🔹 I – Isolation

Isolation ensures that multiple transactions can occur at the same time without interfering with each other.

✅ Example: If two users are booking the last movie ticket, one should succeed and the other should see it as unavailable.

---

## 🔹 D – Durability

Durability guarantees that once a transaction is committed, it will remain so — even in the event of a system failure.

✅ Example: If you receive a confirmation for a purchase, that purchase will persist even if the server crashes afterward.

---

## 🧠 Summary

| Property    | Description                                                                |
|-------------|----------------------------------------------------------------------------|
| Atomicity   | All operations in a transaction succeed or fail as a unit                  |
| Consistency | Transactions preserve data integrity and rules                             |
| Isolation   | Transactions do not interfere with each other                              |
| Durability  | Committed changes survive system failures                                  |

ACID properties are essential to maintaining the reliability, accuracy, and trustworthiness of modern relational databases.

![Image](https://github.com/user-attachments/assets/237e77d7-c02e-4c44-a3b3-6efc672591ab)
