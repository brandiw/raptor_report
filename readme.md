# Raptor Report

More content coming soon!

## What it includes

* Sequelize models and migration for user model
* Settings for Postgresql
* Passport and Passport-Local for authentication
* Express sessions to keep user logged in from page to page
* Connect-Flash for error/success messages
* Bcrypt for hashing passwords

### User Model

| Column Name | SQL Type | Notes |
| ----------- | -------- | ------------------------------- |
| id | Integer | serial primary key |
| createdAt | Date | automatically generated |
| updatedAt | Date | automatically generated |
| firstname | String | - |
| lastname | String | - |
| email | String | usernameField for login |
| password | String | hashed with bcrypt |
| dob | Date | - |

### Routes Supplied

| Method | Path | Location | Purpose |
| ------ | --------------- | -------------------- | ---------------------------- |
| GET | / | index.js | Home page |
| GET | /profile | controllers/profile.js | Profile page (authorization req) |
| GET | /auth/login | controllers/auth.js | Login form page |
| POST | /auth/login | controllers/auth.js | Login submission; Redirect Profile |
| GET | /auth/signup | controllers/auth.js | Signup form page |
| POST | /auth/signup | controllers/auth.js | Signup submission; Redirect Profile |
| GET | /auth/logout | controllers/auth.js | Logout; Redirect Home |
