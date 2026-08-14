# Monorepo Deployment

A hands-on DevOps project demonstrating how to deploy multiple applications from a single monorepo using **GitHub Actions**.

## Stack

* Turborepo + pnpm
* Node.js
* GitHub Actions
* Ubuntu
* PM2
* SSH

## Structure

```text
apps/
├── web
├── http-server
└── ws-server
```

The repository contains a web app, HTTP server, and WebSocket server managed within a single monorepo.

## CI/CD

Separate GitHub Actions workflows handle **staging** and **production** deployments.

```text
Git Push
   ↓
GitHub Actions
   ↓
SSH
   ↓
Server
   ↓
Install & Build
   ↓
PM2 Restart
```
