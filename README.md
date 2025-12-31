# TaskFlow API (Laravel 11)

The backend service for TaskFlow, providing a secure and scalable REST API. It handles data persistence, authentication, and business logic for the Todo application.

## Key Features

- **Authentication:** Secure Token-based auth using **Laravel Sanctum**.
- **Task Management:** Full CRUD for tasks with priority and due dates.
- **Advanced Querying:** Filter by completion status, pagination, and date ranges.
- **Analytics Engine:** Aggregates task data for productivity insights.
- **Database:** Optimized schema with proper indexing for performance.

## API Endpoints

### Authentication
- `POST /api/register` - Create a new user account.
- `POST /api/login` - Authenticate and receive a token.
- `POST /api/logout` - Invalidate current token.

### Tasks
- `GET /api/tasks` - Fetch paginated tasks (supports `?is_completed=true/false`).
- `POST /api/tasks` - Create a new task.
- `PUT /api/tasks/{id}` - Update a task.
- `DELETE /api/tasks/{id}` - permanent delete.

### Analytics & Stats
- `GET /api/tasks/stats` - Quick summary (Total, Completed, Pending).
- `GET /api/tasks/analytics` - Detailed data for charts (Growth, Completion Rates).
- `GET /api/tasks/calendar` - Tasks formatted for calendar view.

## Setup & Installation

1. **Install Dependencies**
   ```bash
   composer install
   ```

2. **Environment Setup**
   Copy the example env file and generate a key.
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

3. **Database Configuration**
   Update `.env` with your database credentials (MySQL or SQLite).

4. **Migrations & Seeding**
   Create tables and populate with test data.
   ```bash
   php artisan migrate --seed
   ```

5. **Run Server**
   ```bash
   php artisan serve
   ```

---

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>
