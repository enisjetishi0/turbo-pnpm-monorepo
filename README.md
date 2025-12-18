# Turbo PNPM Monorepo

## Introduction

A modern monorepo setup using Turborepo and pnpm workspaces. This project demonstrates how to structure a full-stack application with a shared development environment, where both frontend and backend live in the same repository with optimized builds and shared tooling.

---

## Technologies

- **Monorepo**: Turborepo + pnpm workspaces
- **Frontend**: React + Vite + TypeScript
- **Backend**: NestJS + TypeScript
- **Testing**: Vitest + React Testing Library
- **Linting**: ESLint + Prettier
- **Build System**: Turbo (parallel builds with caching)
- **CI/CD**: GitHub Actions
- **Docker**: Multi-stage builds with docker-compose

---

## Features

- Unified development environment for frontend and backend
- Shared TypeScript configurations and types across all packages
- Testing setup with Vitest and React Testing Library
- Pre-commit hooks with Husky and lint-staged
- Parallel build execution with Turborepo
- Fast installs and efficient disk usage with pnpm
- Hot module replacement for both web and API
- TypeScript throughout the entire stack
- Docker support for development and production
- CI/CD with GitHub Actions

---

## How This Project Was Built

- **Monorepo setup**: Configured Turborepo with pnpm workspaces to manage multiple packages
- **Project structure**: Organized into `apps/` (deployable applications) and `packages/` (shared code)
- **Shared tooling**: Created a shared ESLint config that both apps consume
- **Build pipeline**: Set up Turbo tasks for dev, build, and lint with proper dependency ordering
- **TypeScript config**: Base TypeScript configuration extended by each project

---

## How to Run the Project

### Prerequisites

- Node.js 18+ or 20+
- pnpm 9.0.0+

### Setup

1. Click **Code → Download ZIP** on this repository
2. Extract the archive
3. Rename the folder to your project name
4. Open the project folder and initialize Git:

```bash
git init
git add .
git commit -m "Initial project setup"

# Install dependencies
pnpm install

# Run all apps in development mode
pnpm dev

# Build all apps
pnpm build

# Lint all code
pnpm lint
```

### Running Individual Apps

````bash
# Run only the web app
pnp

### Available Scripts

```bash
# Development
pnpm dev          # Run all apps in dev mode
pnpm build        # Build all apps

# Testing
pnpm test         # Run all tests
pnpm test:watch   # Run tests in watch mode
.github/
│   └── workflows/    # GitHub Actions CI/CD
├── apps/
│   ├── api/          # NestJS backend
│   └── web/          # React + Vite frontend
├── packages/
│   ├── eslint-config/      # Shared ESLint configuration
│   ├── typescript-config/  # Shared TypeScript configurations
│   └── types/              # Shared TypeScript types
├── .husky/           # Git hooks
├── docker-compose.yml      # Production Docker setup
├── docker-compose.dev.yml  # Development Docker setup

# Docker
docker-compose up              # Run production build
docker-compose -f docker-compose.dev.yml up  # Run in development mode
```m --filter web dev

# Run only the API
pnpm --filter api dev
````

---

## Project Structure

```
turbo-pnpm-monorepo/
├── apps/
│   ├── api/          # NestJS backend
│   └── web/          # React + Vite frontend
├── packages/
│   └── eslint-config/ # Shared ESLint configuration
├── turbo.json        # Turborepo pipeline configuration
└── pnpm-workspace.yaml # pnpm workspace definition
```

### A short note for contributors

```md
> ℹ️ This repository is a **starter template**.  
> Downloading the ZIP is recommended. Clone only if you intend to contribute.
```
