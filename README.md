# REST API Testing with Python (Requests)

This project demonstrates how to perform basic **CRUD operations** (Create, Read, Update, Delete) on a REST API using Python and the `requests` library.

It uses the public API from **GoRest** to simulate real-world API testing scenarios.

---

## 🚀 Features

* Perform **GET** request to fetch users
* Perform **POST** request to create a new user
* Perform **PUT** request to update user details
* Perform **DELETE** request to remove a user
* Dynamic email generation for unique user creation
* Assertion-based validation for responses

---

## 🛠️ Tech Stack

* Python 3.x
* `requests` library
* JSON handling

---

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

2. Install dependencies:

```bash
pip install requests
```

---

## 🔑 Configuration

Update the following variables in the script before running:

```python
base_url = "https://gorest.co.in"
auth_token = "Bearer YOUR_ACCESS_TOKEN"
```

> ⚠️ **Important:** Replace `YOUR_ACCESS_TOKEN` with your actual GoRest API token.

---

## ▶️ How to Run

Run the script using:

```bash
python your_script_name.py
```

---

## 📌 API Operations Covered

### 1. GET Users

* Endpoint: `/public/v2/users`
* Validates status code `200`

### 2. POST Create User

* Endpoint: `/public/v2/users`
* Generates random email
* Validates:

  * Status code `201`
  * Name correctness

### 3. PUT Update User

* Endpoint: `/public/v2/users/{user_id}`
* Updates user details
* Validates:

  * Status code `200`
  * Updated name

### 4. DELETE User

* Endpoint: `/public/v2/users/{user_id}`
* Validates status code `204`

---

## 🔄 Test Flow

1. Fetch users (GET)
2. Create a new user (POST)
3. Update the created user (PUT)
4. Delete the user (DELETE)

---

## 📧 Random Email Generator

A helper function is used to generate unique email addresses:

```python
def generate_random_email():
```

This prevents duplication errors during user creation.

---

## ✅ Assertions Used

* Status code validation
* Response body verification
* Data integrity checks

---

## 📷 Sample Output

* GET → List of users
* POST → Newly created user with ID
* PUT → Updated user details
* DELETE → Successful deletion (204 No Content)

---

## ⚠️ Notes

* Make sure your API token is valid and active
* API rate limits may apply
* This project is intended for learning and testing purposes

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 👨‍💻 Author

Sachin Tanwar

---

## ⭐ Contribute

Feel free to fork this repository, raise issues, or submit pull requests to improve the project.
