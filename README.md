# Starter Pack Filament

Laravel 13 + Livewire 4 + Filament 5 starter kit.

## Prerequisites

From `composer.json`, this project requires:

- PHP 8.4+
- Composer
- Node.js + yarn
- SQLite (default local database is `database/database.sqlite`)

## Installation

### 1) Clone and enter the project

```bash
git clone <your-repo-url>
cd starter-pack-filament
```

### 2) Run the one-command setup

```bash
composer setup
```

This setup script will:

- install PHP dependencies
- create `.env` from `.env.example` (if missing)
- generate app key
- run migrations
- install Node dependencies
- build frontend assets

## Run in development

Use the combined dev process (app server, queue worker, logs, Vite):

```bash
composer dev
```

## Testing and linting

### Run formatter

```bash
composer lint
```

### Check formatter only (no fixes)

```bash
composer test:lint
```

### Run full test pipeline (clear config + lint check + tests)

```bash
composer test
```

### Run tests directly with Laravel

```bash
php artisan test --compact
```

## Manual setup (if you prefer step-by-step)

```bash
composer install
yarn install
cp .env.example .env
php artisan key:generate
php artisan migrate
yarn build
```

## Common issues

### Vite manifest error

If you see an error like "Unable to locate file in Vite manifest", build or run Vite:

```bash
yarn build
# or
yarn dev
```

### Database errors on first run

Make sure the SQLite file exists and migrations are run:

```bash
touch database/database.sqlite
php artisan migrate
```

