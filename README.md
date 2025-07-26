## Developer Setup

### Dependencies
- PHP ^8.2
- Composer 2.8
- Node.js 22

### Clone Repository

```bash
git clone -b dev https://github.com/vot-ject/vot-ject.git
```

or with ssh. [read this](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

```bash
git clone -b dev git@github.com:vot-ject/vot-ject.git
```

### Installation

1. Install dependencies and build assets:

```bash
cd vot-ject
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

To start the development server, run the following command.

```bash
composer run dev
```

Alternatively, you can run the servers individually.

In one terminal, run the PHP development server:

```bash
php artisan serve
```

In another terminal, run the Vite dev server:

```bash
npm run dev
```