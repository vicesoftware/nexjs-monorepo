<!-- omit in toc -->
# Monorepo Demo

This project demonstrates a monorepo structure with a shared UI component library and a main web application.

## Project Structure

- `demo/`: Contains a sample HTML file to demonstrate the usage of shared components
- `packages/ui/`: Shared UI component library
- `webapp/`: Main web application

## Prerequisites

- Node.js (v14 or later)
- npm (v6 or later)

## Setup

1. Clone the repository and install dependencies:
   ```
   git clone https://github.com/your-username/monorepo-demo.git
   cd monorepo-demo
   npm install
   ```

## Running Everything Together

1. Open three terminal windows

2. In the first terminal, build and serve the UI components:
   ```
   cd packages/ui
   npm run build
   npm run serve-demo
   ```

3. In the second terminal, serve the demo:
   ```
   cd demo
   npx http-server -p 8080
   ```

4. In the third terminal, run the main web application:
   ```
   cd webapp
   npm run dev
   ```

Now you can access:
- The demo at `http://localhost:8080`
- The main web application at `http://localhost:3000`
- The shared components at `http://localhost:5173`

## Rebuilding Shared Components

When making changes to the shared UI components:

1. Navigate to the UI package directory:
   ```
   cd packages/ui
   ```

2. Make your changes to the components

3. Rebuild the UI package:
   ```
   npm run build
   ```

4. The changes will be reflected in both the demo and the main web application

For continuous development, you can use the watch mode:

```
cd packages/ui
npm run build -- --watch
```

This will automatically rebuild the UI package whenever you make changes to the shared components.
