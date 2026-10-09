# Hemora

A Laravel/React application foundation with a proposed property-platform API.

## Current status

Early scaffold. Current routes implement starter authentication, profile/password settings, a welcome page, and an authenticated dashboard. The property, search, analytics, media, and administration API table is a plan, not the current controller surface.

## Features and implementation

- Laravel authentication routes for registration, login, password reset, and email verification.
- Inertia-powered React/TypeScript pages.
- Authenticated dashboard and profile/password settings.
- Starter PHPUnit tests and lint/test workflows.
- A preserved proposed API specification in docs/PLANNED_API.md.

## Technology

PHP >=8.2, Laravel 12, Inertia 2, React, TypeScript, Vite, Tailwind CSS, Composer, and npm.

## Repository map

| Path | Purpose |
| --- | --- |
| [routes/web.php](routes/web.php) | Welcome and dashboard routes |
| [routes/auth.php](routes/auth.php) | Authentication routes |
| [routes/settings.php](routes/settings.php) | Account settings routes |
| [app/Http/Controllers](app/Http/Controllers) | Current controllers |
| [resources/js](resources/js) | React/Inertia interface |
| [tests](tests) | Starter test suite |
| [docs/PLANNED_API.md](docs/PLANNED_API.md) | Proposed future API surface |

## Local setup

```bash
git clone https://github.com/frontend-alex/Hemora.git
cd Hemora
composer install
npm install
cp .env.example .env
php artisan key:generate
```

Choose your local database in .env. If using the default SQLite setup, ensure database/database.sqlite exists before migrating. Then run:

```bash
php artisan migrate
composer run dev
```

composer run dev starts the Laravel server, queue listener, and Vite process. Use the URL printed by the Laravel server.

## Verification

```bash
composer run test
npm run build
npm run types
npm run format:check
```

The repository contains starter tests and workflow files. Test execution and database migration were not performed during this documentation update.

## Limitations and next steps

- The proposed property/search API is not implemented in the current route/controller tree.
- The project is based on the Laravel React starter kit; starter authentication should not be described as a completed property platform.
- Domain models, authorization, search behavior, and acceptance tests remain development work.

## Code review starting points

- [routes/web.php](routes/web.php)
- [routes/auth.php](routes/auth.php)
- [routes/settings.php](routes/settings.php)
- [composer.json](composer.json)
