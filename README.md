## Developer Setup

### Fork the repository

To contribute to the project, you'll need to fork the repository. A fork is a copy of a repository in your own GitHub account. Forking a repository allows you to freely experiment with changes without affecting the original project.

1. On GitHub.com, navigate to the [vot-ject/vot-ject](https://github.com/vot-ject/vot-ject) repository.
2. In the top-right corner of the page, click **Fork**.

<img width="416" height="54" alt="image" src="https://github.com/user-attachments/assets/dde9b9a5-5caa-4c04-af89-695c7a00de36" />

3. Click **Create fork**.

<img width="732" height="557" alt="image" src="https://github.com/user-attachments/assets/edec7cc3-8f3c-4a2a-aed8-631cfc396c68" />

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
