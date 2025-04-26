# PreciselyPRD

A Laravel-based project using Laravel Sail for development.

## Prerequisites

- Docker Desktop
- PHP 8.x
- Composer

## Setup Instructions

1. Clone the repository:
```bash
git clone [repository-url]
cd preciselyprd
```

2. Copy the environment file:
```bash
cp .env.example .env
```

3. Install Composer dependencies:
```bash
composer install
```

4. Generate application key:
```bash
php artisan key:generate
```

5. Start the Docker environment with Laravel Sail:
```bash
./vendor/bin/sail up -d
```

6. Run database migrations:
```bash
./vendor/bin/sail artisan migrate
```

7. Install and build frontend assets:
```bash
./vendor/bin/sail npm install
./vendor/bin/sail npm run dev
```

## Development

The application will be available at: https://preciselyprd.beginly.test

### Port Configuration

The following ports are configured by default:
- Main Application: 8199 (SSL enabled)
- Database: 5499
- Redis: 6499
- Mailpit: 1099 (Dashboard: 8099)
- MinIO: 9999 (Console: 8999)
- Vite: 5200

### Useful Commands

- Start all services: `./vendor/bin/sail up -d`
- Stop all services: `./vendor/bin/sail down`
- Run tests: `./vendor/bin/sail test`
- Run artisan commands: `./vendor/bin/sail artisan [command]`
- Access database: `./vendor/bin/sail psql`

## Environment Configuration

Key configuration points in your `.env` file:

- `APP_URL`: Set to https://preciselyprd.beginly.test
- `DB_CONNECTION`: PostgreSQL is used as the database
- `REDIS_HOST`: Redis for caching
- `MAIL_HOST`: Mailpit for local email testing
- `WORKOS`: Configure WorkOS for authentication

## Support

For any questions or issues, please [create an issue](repository-issues-url).
