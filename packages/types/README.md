# @repo/types

Shared TypeScript types and interfaces used across the monorepo.

## Usage

```typescript
import { User, ApiResponse, PaginatedResponse } from '@repo/types';

const user: User = {
  id: '1',
  email: 'user@example.com',
  name: 'John Doe',
  createdAt: new Date(),
  updatedAt: new Date(),
};

const response: ApiResponse<User> = {
  success: true,
  data: user,
};
```

## Adding New Types

Add your types to `src/index.ts` and export them:

```typescript
export interface YourType {
  // your fields
}
```
