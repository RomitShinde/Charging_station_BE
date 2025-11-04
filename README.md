# Charging Station — Backend

Concise instructions to set up and run the NestJS backend locally (Windows PowerShell examples).
- Used NestJS for backend application
- You can find admin credentials inside folder path charging_station_be\src\auth\auth.service.ts which are added static.
- Download Pg Admin4 and latest postgre SQL 18.0.2 latest version and do all necessary installations for backend.

## Requirements

- Node.js 18+ (or supported LTS)
- yarn (or npm)
- (Optional) PostgreSQL if you plan to run with TypeORM and the `pg` driver

## Quick start

1. Clone the repo and enter the folder:

```powershell
git clone <repo-url> .
cd d:\ChargingStation\charging_station_be
```

2. Install dependencies (using yarn):

```powershell
yarn install
```

Alternatively you can use npm:

```powershell
npm install
```

3. Configure environment (optional / app-specific):

- Create a `.env` file in the project root if you need to supply DB or port settings.
- Common variables the app may use:

```
PORT=3000
DB_HOST=localhost
DB_PORT=5432
DB_USER=postgres
DB_PASSWORD=yourpassword
DB_NAME=charging_db
```

Note: This project uses TypeORM (`typeorm`, `pg`). If you don't configure DB env variables and your code expects a DB connection, startup may fail.

## Run (development)

Start the backend in watch mode (recommended during development):

```powershell
yarn start:dev
```

Or with npm:

```powershell
npm run start:dev
```

This will run the NestJS app and automatically reload on changes. By default the app listens on `process.env.PORT` or `3000`.
