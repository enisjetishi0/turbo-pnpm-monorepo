# @repo/typescript-config

Shared TypeScript configurations for the monorepo.

## Usage

### For React/Vite apps:

```json
{
  "extends": "@repo/typescript-config/react.json"
}
```

### For Node/NestJS apps:

```json
{
  "extends": "@repo/typescript-config/node.json"
}
```

## Available Configs

- `base.json` - Base TypeScript configuration with strict settings
- `react.json` - Configuration for React applications
- `node.json` - Configuration for Node.js applications with decorators support
