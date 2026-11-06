# Full-Stack Kanban

A React and Express kanban prototype with board and card APIs, SQLite storage, calendar routes, search, and saved views.

The application lives under projects/kanban-app. The package's dev script starts Vite only; the Express entry point must be started separately for API-backed behavior.

## Start reading

- [`projects/`](projects/)

## Development

Use Node.js and npm compatible with the versions recorded in the package manifest and lockfile. Each package is installed from its own directory.

Start this package from the repository root:

```sh
cd projects/kanban-app
npm ci
npm run dev
```

Additional scripts in this package: `npm run build`, `npm run lint`.

## Configuration

The source reads `DB_PATH`. Supply environment-specific values locally. Browser-exposed settings such as `VITE_` and `NEXT_PUBLIC_` variables are public configuration, not a place for private credentials.

## Start the API

After installing the nested package, open a second terminal in `projects/kanban-app` and run `npx tsx server/index.ts`. The Express API defaults to port 3001 and runs its local SQLite migrations on startup. Keep it running alongside Vite.
