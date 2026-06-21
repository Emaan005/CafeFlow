CafeFlow — Bakery Management System

A full-stack bakery management system built twice on different technology stacks to compare relational and NoSQL database architectures against the same product requirements.


Overview

CafeFlow was developed as part of two separate university courses — a Web Engineering course (Laravel/MySQL) and an Advanced Database course (Flask/MongoDB). Building the same system twice with different backends made the architectural trade-offs between relational and document-oriented databases directly observable.


Versions

Version 1 — Relational (Laravel + MySQL)

BackendPHP / LaravelDatabaseMySQLArchitectureMVC, normalized relational schema

Version 2 — NoSQL (Flask + MongoDB)

BackendPython / FlaskDatabaseMongoDBArchitectureDocument-oriented, embedding vs. referencing strategies


Features

Admin Panel


Inventory management (add, update, remove items)
Order tracking and status management
Dashboard overview


Customer Panel


Browse available products
Place and manage orders
Checkout flow



What I learned

The most valuable part of this project was reasoning about the same data model in two paradigms:


In MySQL, data is normalized across tables with foreign keys — clean for complex queries, requires JOINs
In MongoDB, related data can be embedded in a single document or referenced — better read performance for certain access patterns, but requires careful design upfront


Deciding when to embed vs. reference in MongoDB (e.g. embedding order items directly in an order document vs. referencing a separate products collection) forced a level of data-access thinking that a single-stack project wouldn't have surfaced.


Project Structure

cafeflow/
├── laravel-mysql/        # Version 1 — PHP/Laravel + MySQL
│   ├── app/
│   ├── database/
│   └── ...
└── flask-mongodb/        # Version 2 — Python/Flask + MongoDB
    ├── app/
    ├── models/
    └── ...


Setup

Laravel / MySQL version

bashcd laravel-mysql
composer install
cp .env.example .env
# Configure your MySQL credentials in .env
php artisan migrate
php artisan serve

Flask / MongoDB version

bashcd flask-mongodb
pip install -r requirements.txt
# Configure your MongoDB URI in .env or config.py
python app.py




VersionCourseLaravel/MySQLWeb EngineeringFlask/MongoDBAdvanced Database Systems

University: COMSATS University Islamabad, Wah Campus
