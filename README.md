## Employees Management Application BY JUSTIN MOREYL (Янюшкин Вадим)
[![N|Solid](https://i.ibb.co/vHpsNKL/logo.png)](https://nodesource.com/products/nsolid)
## Definition

- Laravel + vue.js




## Technologies
- [Composer] - it is an application level batch manager for the PHP programming language
- [Laravel-8] - free open source web framework designed for development using the MVC architectural model.
- [Vue.js] - Vue.js - open source JavaScript framework
- [MySQL-5] - free relational database management system
- [HTML-5] - structuring language
- [bootstrap 4] - free set of tools for creating websites and web applications.

## Specification

1. Use Laravel 8 framework as development platform
2. Mysql 5 or later database
3. Vue.js + Laravel mix for compiling assets (js, css and images)
   3.1 Implement vue,js on employee management only. CRUD + search features
4. Bootstrap

>  USER INTERFACE
1. Interface should be responsive based on HTML5 and bootstrap 4.
2. User interface layout should have side bar menu and header
- On side bar the following should be displayed as vertical menu
  2.1 Dashboard
  2.2 Employee management
  3.2 System management
  3.2.1 Country (sub menu)
  3.2.2 State (sub menu)
  3.2.3 City (sub menu)
  3.2.4  Department(sub menu)
4. User Management
   4.1 User (sub menu)
   4.2 Role (sub menu optional)
   4.3 Permission (sub menu optional)

5. On header interface, display the name of the logged in user as well as the menu for logout
6. After authentication, the user should be redirected to blank dashboard

>Authentication
- User will be able to login using email and password
- Three(3) failed attempt will lock the user for 5 minutes
1. User Management
- Create, Update and Delete users
- Change Password
- Search User by username and email
- Role & Permission – CRUD (optional)
2. Employee management
- List of employees with search and filter by employee name and department
- Create, update and delete employees

3. System Management
   3.1 Country
- List of countries
- Create, Update and delete
  3.2 State
- List of states
- Create, Update and delete
  3.3 City
- List of cities
- Create, Update and delete
  3.4 Department
- List of departments
- Create, Update and delete

> API
- Create an API and point for user registration and authentication
- Create an API and point to list all employees order alphabetically by lastname

> Data Dictionary
- Employees
  | Id | Auto increment |  
  | lastname | varchar(60) | *required |
  | firstname | varchar(60) | *required |
  | middle name | varchar(60) |
  | address | varchar(120) | *required |
  | department_id | Foreign key | *required |
  | city_id | Foreign keyt | *required |
  | state_id | Foreign key | *required |
  | country_id | Foreign key | *required |
  | zip_code | char(10) | *required |
  | birthdate | date |
  | date_hired | date |
  | created_at | datetime |
  | updated_at | datetime |
  | deleted_at |datetimet |
- Users
  | Id | Auto increment |  
  | username | char(20) | *required |
  | lastname | varchar(60) | *required |
  | email | varchar(60) | *required |
  | password | varchar(60) | *required |
  | created_at | datetime |
  | updated_at | datetime |
  | deleted_at |datetimet |
- Countries
  | Id | Auto increment |  
  | country_code | char(20) | *required |
  | name | varchar(60) | *required |
  | created_at | datetime |
  | updated_at | datetime |
  | deleted_at | datetimet |
- States
  | Id | Auto increment |
  | country_id | Foreign key | *required |
  | name | varchar(60) | *required |
  | created_at | datetime |
  | updated_at | datetime |
  | deleted_at |datetimet |
- Cities
  | Id | Auto increment |
  | state_id | Foreign key | *required |
  | name | varchar(60) | *required |
  | created_at | datetime |
  | updated_at | datetime |
  | deleted_at | datetimet |
- Departments
  | Id | Auto increment |
  | department_id | Foreign key | *required |
  | name | varchar(60) | *required |
  | created_at | datetime |
  | updated_at | datetime |
  | deleted_at | datetimet |


## Development

Want to contribute? Great!


Open your favorite Terminal and run First Tab:

First Tab:

```sh
npm install && npm run dev
```
Config your .env file and run second tab:
```sh
php artisan migrate
```
Run next tab:
```sh
php artisan serve 
```

Open your second Terminal and run these commands for mix vue.js + laravel 8.

```sh
npm run watch
```

App running at:
http://127.0.0.1:8000

Thank you enjoy!

## License

MIT
