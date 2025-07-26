## Developer Setup

### Dependencies
- PHP ^8.2
- Composer 2.8
- Node.js 22

### Installation

1. Install dependencies and build assets:

```bash
composer install
npm install
npm run build
```

2. Run database migrations:

```bash
php artisan migrate --seed
```

3. Copy the environment file and generate an app key:

```bash
cp .env.example .env
php artisan key:generate
```
*Make sure to configure your `.env` file, especially the database connection.*

### Running the Project

```bash
composer run dev
```