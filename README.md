<!-- omit in toc -->
# Monorepo Demo

This project demonstrates a monorepo structure with a shared UI component library and a main web application.

- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Running the Demo](#running-the-demo)
- [Running the Main Web Application](#running-the-main-web-application)
- [Developing Shared Components](#developing-shared-components)
- [Running Everything Simultaneously](#running-everything-simultaneously)
- [Continuous Development](#continuous-development)


## Project Structure

- `demo/`: Contains a sample HTML file to demonstrate the usage of shared components
- `packages/ui/`: Shared UI component library
- `webapp/`: Main web application

## Prerequisites

- Node.js (v14 or later)
- npm (v6 or later)
- http-server (or any similar static file server)

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/your-username/monorepo-demo.git
   cd monorepo-demo
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Install http-server globally (if not already installed):
   ```
   npm install -g http-server
   ```

## Running the Demo

To run the demo sample app:

1. Build the UI components:
   ```
   cd packages/ui
   npm run build
   ```

2. Serve the demo using http-server:
   ```
   cd ../../demo
   http-server
   ```

3. Open your browser and navigate to `http://localhost:8080`

## Running the Main Web Application

To run the main web application:

1. Navigate to the webapp directory:
   ```
   cd webapp
   ```

2. Start the development server:
   ```
   npm run dev
   ```

3. Open your browser and navigate to `http://localhost:3000`

## Developing Shared Components

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

4. To see your changes in the demo, restart the http-server in the demo directory

5. To see your changes in the main web application, restart the development server in the webapp directory

## Running Everything Simultaneously

To run both the demo and the main web application simultaneously:

1. Open three terminal windows

2. In the first terminal, navigate to the UI package and build it:
   ```
   cd packages/ui
   npm run build
   ```

3. In the second terminal, serve the demo:
   ```
   cd demo
   http-server
   ```

4. In the third terminal, run the main web application:
   ```
   cd webapp
   npm run dev
   ```

Now you can access the demo at `http://localhost:8080` and the main web application at `http://localhost:3000`.

## Continuous Development

For continuous development of shared components:

1. In one terminal, watch for changes in the UI package:
   ```
   cd packages/ui
   npm run build -- --watch
   ```

2. In another terminal, run the demo or the main web application as described above

This setup will automatically rebuild the UI package whenever you make changes to the shared components.
