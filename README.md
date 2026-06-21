# CafeFlow — Bakery Management System

A full-stack bakery management system built **twice** on different technology stacks to compare relational and NoSQL database architectures against the same product requirements.

---

## Overview

CafeFlow was developed as part of two separate university courses — a Web Engineering course (Laravel/MySQL) and an Advanced Database course (Flask/MongoDB). Building the same system twice with different backends made the architectural trade-offs between relational and document-oriented databases directly observable.

---

## Versions

### Version 1 — Relational (Laravel + MySQL)
| | |
|---|---|
| **Backend** | PHP / Laravel |
| **Database** | MySQL |
| **Architecture** | MVC, normalized relational schema |

### Version 2 — NoSQL (Flask + MongoDB)
| | |
|---|---|
| **Backend** | Python / Flask |
| **Database** | MongoDB |
| **Architecture** | Document-oriented, embedding vs. referencing strategies |

---

## Features

**Admin Panel**
- Inventory management (add, update, remove items)
- Order tracking and status management
- Dashboard overview

**Customer Panel**
- Browse available products
- Place and manage orders
- Checkout flow

---

## What I Learned

- In **MySQL**, data is normalized across tables with foreign keys — clean for complex queries, requires JOINs
- In **MongoDB**, related data can be embedded or referenced — better read performance for certain access patterns, but requires careful design upfront
- Deciding when to embed vs. reference in MongoDB forced a level of data-access thinking that a single-stack project wouldn't have surfaced

---

## Project Structure
cafeflow/

├── laravel-mysql/        # Version 1 — PHP/Laravel + MySQL

│   ├── app/

│   ├── database/

│   └── ...

└── flask-mongodb/        # Version 2 — Python/Flask + MongoDB

├── app/

├── models/

└── ...

---

## Setup

### Laravel / MySQL version
```bash
cd laravel-mysql
composer install
cp .env.example .env
# Configure your MySQL credentials in .env
php artisan migrate
php artisan serve
```

### Flask / MongoDB version
```bash
cd flask-mongodb
pip install -r requirements.txt
# Configure your MongoDB URI in .env or config.py
python app.py
```

---

## Course Context

| Version | Course |
|---|---|
| Laravel/MySQL | Web Engineering |
| Flask/MongoDB | Advanced Database Systems |

**University:** COMSATS University Islamabad, Wah Campus
