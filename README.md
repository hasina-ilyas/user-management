
# User Management Software

This Laravel-based User Management Software provides an efficient way to manage users and roles with an intuitive interface.

## Features
- Role-based access control.
- User management system.
- Admin panel for role and permission management.

---

## Requirements

Ensure your system meets the following prerequisites before installation:

- **PHP**: >= 8.0
- **Composer**: Latest version
- **Database**: MySQL, PostgreSQL, or SQLite
- **Node.js**: >= 16.x
- **NPM/Yarn**: Latest version
- **Web Server**: Apache or Nginx

---

## Installation

Follow these steps to install and configure the application:

### 1. Clone the Repository
```bash
git clone https://github.com/hasina-ilyas/user-management.git
cd user-management
```

### 2. Install Dependencies
Install PHP dependencies:
```bash
composer install
```

Install JavaScript dependencies:
```bash
npm install
```
Or, if using Yarn:
```bash
yarn install
```

### 3. Configure the Environment
Copy the `.env.example` file to `.env`:
```bash
cp .env.example .env
```

Edit the `.env` file and update the following variables to match your environment:
```env
APP_NAME=UserManagementSoftware
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

Generate the application key:
```bash
php artisan key:generate
```

### 4. Set Up the Database
Run migrations to create the required tables:
```bash
php artisan migrate
```

(Optional) Seed the database with default roles and users:
```bash
php artisan db:seed
```

### 5. Compile Frontend Assets
Compile the CSS and JavaScript files:
```bash
npm run dev
```
For production:
```bash
npm run build
```

### 6. Start the Server
Start the development server:
```bash
php artisan serve
```

Access the application at `http://localhost:8000`.

---

## Additional Configuration

### Role Management
- Use the admin panel at `/admin/roles` to manage roles and permissions.

### Cache Configuration
For better performance, cache the configuration:
```bash
php artisan config:cache
```

---

## Troubleshooting

- **Database Errors**: Ensure database credentials in the `.env` file are correct.
- **Assets Not Loading**: Make sure you’ve run `npm run dev` or `npm run build`.
- **Missing `.env` file**: Recreate it by copying `.env.example`.

---

## License

This project is open-source and available under the [MIT License](LICENSE).
