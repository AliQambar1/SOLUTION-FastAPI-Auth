<<<<<<< HEAD
# Python FastAPI Serializers and Controllers Lab Solution

## About

This repo contains the solution code for the [Python FastAPI Serializers and Controllers Lab](https://pages.git.generalassemb.ly/modular-curriculum-all-courses/python-fastapi-serializers-and-controllers-lab/canvas-landing-pages/fallback.html)

## Getting Started

1. Fork and clone this repo.

2. Navigate into the project directory:

```sh
 cd python-fastapi-serializers-and-controllers-lab-solution
```

3. Install dependencies (this also creates the virtual environment if it doesn’t exist):

```sh
 pipenv install
```

4. Activate the virtual environment:

```sh
 pipenv shell
```

5. Set up your PostgreSQL database:

   - Ensure PostgreSQL is installed and running on your machine.
   - Create a database named `teas_db` if it does not already exist:

```bash
createdb teas_db
```

6. Open the application in Visual Studio Code:

```bash
code .
```

7. The database connection string is defined in the `config/environment.py` file:

```python
db_URI = "postgresql://<username>@localhost:5432/teas_db"
```

> _Modify your database connection string to use your username as the `<username>`._

8. Seed the database with initial data:

   - Run the `seed.py` file to reset the database by dropping existing tables and repopulating it with starter data:

```bash
pipenv run python seed.py
```

> You should see output indicating the database was successfully seeded. If there are any errors, check the `db_URI` in the `config/environment.py` file.

9. Start the development server:

```bash
pipenv run uvicorn main:app --reload
```

> You should now have the app running. Visit [`http://127.0.0.1:8000`](http://127.0.0.1:8000) in your browser to confirm it’s working.

10. Now you can test each endpoint using FastAPI’s built-in documentation.

> Navigate to FastAPI Documentation: Open [`http://localhost:8000/docs`](http://localhost:8000/docs) in your browser.

<br>

### Troubleshooting PostgreSQL

- The database connection string is defined in the `config/environment.py` file:

  ```python
  db_URI = "postgresql://<username>@localhost:5432/teas_db"
  ```

- Ensure your PostgreSQL instance is configured to allow connections with the provided credentials.
- **_Modify your database connection string to use your username as the `<username>`._**

#### Setting Up a User in PostgreSQL

To connect to a specific PostgreSQL user, use the following command:

```sh
psql -U <username>
```

#### Handling "Role Does Not Exist" Error

If you see this error:

```sh
Error: FATAL: role "<username>" does not exist
```

it means that the specified user does not exist in PostgreSQL.

#### Creating a New PostgreSQL User

To create the user, run the following command inside `psql`:

```sql
CREATE ROLE "<username>" WITH LOGIN PASSWORD 'your_secure_password';
```

> 🔹 **Replace** `<username>` with your desired username and **choose a secure password**.

This will allow you to connect using one of the following database connection strings:

#### Connection Strings:

If **no password is required**:

```python
db_URI = "postgresql://<username>@localhost:5432/teas_db"
```

If **a password is required**:

```python
db_URI = "postgresql://<username>:<your_secure_password>@localhost:5432/teas_db"
```

This ensures that PostgreSQL correctly authenticates and allows access to the `teas_db` database.
=======
# Aurevia – Car Marketplace & Auction Platform

## 📌 Project Overview
Aurevia is a car marketplace platform where **admins** can list cars for sale and manage auctions, while **users** can browse cars, send inquiries, and participate in auctions.

---

## 👤 User Stories

### 🔹 Authentication
1. As a new user, I want to create an account so I can access platform features.
2. As a registered user, I want to log in securely to manage my account.
3. As a logged-in user, I want to log out to keep my account secure.

---

### 🔹 Cars
4. As a user, I want to view all listed cars so I can explore available options.
5. As a user, I want to distinguish between available and sold cars.
6. As a user, I want to view detailed information about a car (model, price, specifications).

---

### 🔹 Inquiries
7. As a user, I want to send an inquiry about a car to contact the admin.

---

### 🔹 Auctions
8. As a user, I want to participate in car auctions by placing bids.
9. As a user, I want to view the highest bid and auction status.

---

## 🛠️ Admin Stories

1. As an admin, I want to log in securely.
2. As an admin, I want to add new car listings.
3. As an admin, I want to edit existing car details.
4. As an admin, I want to update car status (available / sold).
5. As an admin, I want to create and manage auctions.
6. As an admin, I want to monitor bids to ensure fair auctions.

---

## 🗺️ System Design

### Routes
![Routes image](Routes.png)

### UI Preview
![Screenshot]()

---

## Wireframes
....

---

## Database Relationship Diagram
https://lucid.app/lucidchart/e70eb819-35d4-421e-97c1-e4aa77354bea/edit





>>>>>>> 76fe52b (Adding Readme and Authentication and Authorization)
