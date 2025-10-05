
# 📚 MongoDB Data Layer Fundamentals — Week 1

This project demonstrates basic and advanced MongoDB operations using both the **MongoDB Shell (`mongosh`)** and **MongoDB Compass**.  
It covers:
- Installation & setup
- Inserting sample data
- Performing CRUD operations
- Running advanced queries & aggregation pipelines
- Implementing indexes for performance

The project uses a database called **`plp_bookstore`** and a collection named **`books`**.

---

## 🛠️ Requirements

Make sure you have the following installed on your machine:

- [Node.js](https://nodejs.org) (v16+)
- [MongoDB Community Edition](https://www.mongodb.com/try/download/community)
- [MongoDB Shell (`mongosh`)](https://www.mongodb.com/docs/mongodb-shell/install/)
- [MongoDB Compass](https://www.mongodb.com/products/compass) (GUI client)

---

## 📂 Project Structure

```

.
├── insert_books.js   # Script to populate the database with sample data
├── queries.js        # MongoDB shell queries
├── README.md         # Project documentation

```

---

## 🚀 How to Run the Project

### 1. **Start MongoDB Service (Windows)**

If you're facing connection errors, your MongoDB service may not be running.  
You can start it manually using `services.msc`:

1. Press **Win + R**
2. Type:
```

services.msc

```
and press **Enter**
3. In the Services window, scroll to find:
```

MongoDB Server (MongoDB)

```
4. Right-click it → **Start**  
(or **Restart** if it’s already running)

Once started, MongoDB will be available at:
```

mongodb://127.0.0.1:27017

````

---

### 2. **Insert Sample Data**

Open **Command Prompt** in your project folder and run:

```bash
node insert_books.js
````

This will insert at least 10 sample book documents into the `books` collection of the `plp_bookstore` database.

---

### 3. **Run Queries Using mongosh**

Start MongoDB shell:

```bash
mongosh
```

Switch to the database:

```javascript
use plp_bookstore
```

Run any queries manually, for example:

```javascript
db.books.find().pretty()
db.books.find({ genre: "Fiction" }).pretty()
```

Or run **all the queries** in `queries.js` automatically:

```bash
mongosh < queries.js
```

---

### 4. **Explore Data Using MongoDB Compass**

You can also use MongoDB Compass for a GUI experience:

1. Open **MongoDB Compass**
2. In the connection string field, enter:

   ```
   mongodb://127.0.0.1:27017
   ```
3. Click **Connect**
4. In the sidebar, click on the **`plp_bookstore`** database → select the **`books`** collection

From here you can:

* Browse data visually
* Run filter queries using JSON
* Create and view indexes
* Build aggregation pipelines with a drag-and-drop interface

---

## 🧠 Troubleshooting

### ❌ `mongosh` not connecting / ECONNREFUSED

* Start MongoDB using `services.msc` (as shown above)
* Check that port **27017** is available
* Try connecting manually:

  ```bash
  mongosh mongodb://127.0.0.1:27017
  ```

### ❌ “Cannot find module 'mongodb'” in Node

Install the MongoDB Node.js driver:

```bash
npm install mongodb
```

Then re-run the script.

---

## 🧪 Expected Outcome

* A working MongoDB database with properly structured book data
* Successful CRUD and advanced query execution
* Working aggregation pipelines
* Indexed fields with performance improvements shown via `explain()`
* Visual confirmation of your data in **MongoDB Compass**

---

## 📝 How to Clone and Run



```bash
git clone https://github.com/PLP-MERN-Stack-Development/mongodb-data-layer-fundamentals-and-advanced-techniques-375516521.git
cd mongodb-data-layer-fundamentals-and-advanced-techniques-375516521.git
node insert_books.js
mongosh < queries.js
```

Then open **MongoDB Compass** to explore the data.

---

## ✨ Author

* CHARLES WAMBUA
 — MongoDB Data Layer Fundamentals
* PLP MERN Project

```

