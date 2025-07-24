# 💸 Cash Flow Minimizer System

This system reduces the *number of transactions* among multiple banks that use *different payment modes, ensuring smooth interbank settlements. A central **World Bank* acts as a mediator for banks that don’t share common payment methods.

---

## 🚀 Getting Started

Let's assume we have 6 banks:

1. Central_Bank (World Bank with all payment modes)
2. Bank_A
3. Bank_B
4. Bank_C
5. Bank_D
6. Bank_E

### 💰 Sample Transactions

| Debtor        | Creditor      | Amount |
|---------------|---------------|--------|
| Bank_E        | Central_Bank  | Rs 100 |
| Bank_E        | Bank_A        | Rs 300 |
| Bank_E        | Bank_B        | Rs 100 |
| Bank_E        | Bank_C        | Rs 100 |
| Bank_D        | Central_Bank  | Rs 300 |
| Bank_D        | Bank_B        | Rs 100 |
| Central_Bank  | Bank_A        | Rs 400 |
| Bank_A        | Bank_B        | Rs 200 |
| Bank_B        | Bank_C        | Rs 500 |

📌 These form a *directed graph* of debts:

![Graph](https://user-images.githubusercontent.com/54183085/110007387-9c625100-7d40-11eb-9128-29073ea4b3f3.png)

---

## 🏦 Payment Mode Restrictions

Each bank supports only certain modes of payment:

- Central_Bank – Google Pay, AliPay, Paytm
- Bank_A – Google Pay, AliPay
- Bank_B – AliPay
- Bank_C – Google Pay, Paytm
- Bank_D – AliPay, Paytm
- Bank_E – Paytm

A bank can only *send/receive payments* via its supported methods. The *Central Bank supports all*, so it serves as an intermediary when two banks have no payment method in common.

---

## 🧠 Algorithm (Greedy Approach)

1. *Calculate Net Amounts*:
2. *Pick the Max Debtor (X)* and *Max Creditor (Y)* with a *common payment mode*.
3. Settle the *minimum* of their net amounts (min(abs(x), y)).
4. Adjust balances and *repeat* until all debts are cleared.

### 🧾 Example Output:
The algorithm will output the *minimum required transactions* between compatible banks while using the fewest possible steps.

---

## 🛠 Technologies Used
- *C++*
- STL (vector, set, unordered_map)
- Graphs & Greedy Algorithms

---

## 👨‍💻 Notes

- This project is built by a beginner as a learning project.
- All names used are fictional and represent general banking scenarios.

---

## 📎 License

This project is open source and free to use for educational purposes.
