# Setup

Initialize refine-app inside `refine` container.

```
docker-compose exec refine bash
```

```
npm create refine-app@latest
```

# vite config

`server.host: true` is required to be able to access from outside the container.

vite.config.ts

```typescript
import react from "@vitejs/plugin-react";
import { defineConfig } from "vite";

export default defineConfig({
  server: {
    host: true,
  },
  plugins: [react()],
});
```

# graphql client config

App.tsx

```typescript
const API_URL = "http://localhost:8080/v1/graphql";

const client = new GraphQLClient(API_URL, {
  headers: {
    "x-hasura-admin-secret": "mymyadminsecretkey",
    "x-hasura-role": "admin",
    "content-type": "application/json",
  },
});
```
