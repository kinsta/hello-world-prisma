![Prisma](https://user-images.githubusercontent.com/2342458/236766510-6bdddf7d-a726-4a73-8fcd-51bfc84de452.png)

# Kinsta - Hello World - Prisma

An example of how to deploy a **Prisma + Next.JS** application on Kinsta.

---
Kinsta is a developer-centric cloud host / PaaS. We’re striving to make it easier for you to share your web projects with your users. Focus on coding and building, and we’ll take care of deployment and provide fast, scalable hosting. + 24/7 expert-only support.

- [Start your free trial](https://kinsta.com/signup/?product_type=app-db)
- [Application Hosting](https://kinsta.com/application-hosting)
- [Database Hosting](https://kinsta.com/database-hosting)

## Installation
This application requires a Database to work. So before you'll start you have to set up a **PostgresSQL** database. We recommend using [Kinsta Database Hosting](https://kinsta.com/database-hosting) for this task. Before continuing make sure you have the connection string - it should look like this `postgresql://username:password@your_postgres_db.cloud/db_identifier`.

If you are using **Kinsta Database Hosting** make sure you set up the internal connection by following [this guide](https://kinsta.com/docs/adding-internal-connections/).

### Environment Variables
```DB_CONNECTION_URL``` - paste the database connection string here.

## Dependency Management
Kinsta automatically installs dependencies defined in your `package.json` file during the deployment process.

## Web Server Setup

### Port

Kinsta automatically sets the `PORT` environment variable. You should **not** define it yourself and you should **not** hard-code it into the application.

### Start Command

When deploying an application, Kinsta automatically creates a web process with `npm start` as the entry point. Make sure to use this command to run your server.

## Deployment Lifecycle

Whenever a deployment is initiated (through creating an application or re-deploying due to an incoming commit) the `npm build` command is run, followed by the `npm start` command.

## What is Prisma
Prisma is an open-source database toolkit that simplifies database access for developers by providing a type-safe and intuitive API. It supports multiple databases and generates efficient, optimized SQL queries for faster performance. More information is available on the [prisma.io](https://www.prisma.io/) website.
