# 🔎 Data Vault Explorer

**Data Vault Explorer** is an interactive, single-file web application designed to help you **understand and explore a Data Vault model visually**.
It combines schema visualization, relationship exploration, and model insights in a clean, modern interface — all directly in the browser.

No build tools. No backend. Just open the file and explore.

```
/screenshots/dv_main.png
```


---

# ✨ Features

* 🧭 **Interactive ER Diagram**
  Visually explore hubs, satellites, links, and other Data Vault entities in a clear, structured diagram.

* 📊 **Model Insights**
  Built-in charts and summaries help you quickly understand the structure and distribution of the model.

* 🔍 **Relationship Exploration**
  Easily inspect how entities connect across the vault.

* 🛠 **Pipeline Guidance**
  A dedicated tab outlines the **recommended development pipeline**, helping teams move from source systems to a complete Data Vault model.

* 📁 **Single-File App**
  Everything runs from one HTML file — perfect for sharing, demos, or documentation.

---

# 🗂️ Interface Overview

The application is organized into simple tabs that each focus on a different aspect of the model:

| Tab                     | What it helps you do                                                                   |
| ----------------------- | -------------------------------------------------------------------------------------- |
| 🧩 **Model Diagram**    | Explore the Data Vault structure visually through an interactive ER diagram.           |
| 📊 **Insights**         | View high-level statistics and charts about the model.                                 |
| 🔗 **Relationships**    | Understand how hubs, links, and satellites connect.                                    |
| 🛠 **Pipeline**         | Follow a recommended, actionable path for building and extending the Data Vault model. |
| 📘 **Reference / Help** | Quick explanations of Data Vault components and conventions.                           |

---

# 🛠 Pipeline – From Source to Data Vault

The **Pipeline** tab provides a practical roadmap for developing and extending a Data Vault model.
Instead of focusing only on structure, it highlights **how to build the model step by step**.

Typical stages include:

### 1️⃣ Identify Source Entities

Start by identifying the **core business entities** in your source systems.
These usually become **Hubs** in the Data Vault.

Examples:

* Customer
* Order
* Product

---

### 2️⃣ Define Business Keys

For each entity, determine the **stable business key** that uniquely identifies it across systems.

Example:

```
CUSTOMER_ID
ORDER_NUMBER
PRODUCT_CODE
```

These keys will become the primary identifiers for **Hub tables**.

---

### 3️⃣ Create Hubs

Create **Hub tables** to store the business keys and their metadata (load date, source system, hash key).

Hubs represent **core business concepts** and should remain stable over time.

---

### 4️⃣ Create Links

Define **Links** to represent relationships between hubs.

Examples:

* Customer ↔ Order
* Order ↔ Product

Links capture **associations between business entities**.

---

### 5️⃣ Add Satellites

Attach **Satellites** to Hubs or Links to store descriptive attributes and historical changes.

Typical satellite contents:

* Descriptive attributes
* Timestamps
* Source system metadata

Satellites enable **full history tracking** without altering hubs or links.

---

### 6️⃣ Expand Iteratively

Data Vault models are designed to **grow incrementally**.

The pipeline helps identify:

* missing satellites
* potential links
* new hubs from additional source systems

This supports **agile, iterative warehouse development**.

---

# 🚀 Getting Started

1. Download or clone this repository.
2. Open the file:

```bash
data-vault-explorer.html
```

3. The application runs directly in your browser.

No installation or server required.

---

# 🛠 Tech Stack

* **HTML5**
* **CSS3**
* **Vanilla JavaScript**
* **Chart.js** for visual analytics

---

# 💡 Use Cases

This tool is useful for:

* 📚 **Learning Data Vault modeling**
* 🧑‍🏫 **Training or workshops**
* 🧭 **Exploring complex warehouse schemas**
* 📊 **Documentation for data teams**
* 🎤 **Architecture demos**

---

# 📸 Preview

```
/screenshots/dv_er.png
/screenshots/dv_complexity.png
/screenshots/dv_loading_pipeline.png
/screenshots/dv_decision_making.png
```

---

# 📄 License

MIT License — feel free to use, modify, and share.

---

⭐ If you find this useful, consider starring the repository.
