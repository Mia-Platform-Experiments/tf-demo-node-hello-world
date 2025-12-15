# tf-demo-node-hello-world

Simple Node.js hello world application for Azure App Service deployment.

## Local Development

### Prerequisites

- Node.js 18.x or higher
- npm

### Setup and Run

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the server:**
   ```bash
   npm start
   ```

3. **Test the application:**
   ```bash
   # Hello endpoint
   curl http://localhost:8080/
   
   # Health check
   curl http://localhost:8080/health
   ```

The server runs on port `8080` by default (or the port specified in `PORT` environment variable).

### Expected Response

```json
{
  "message": "Hello World from Node.js!",
  "timestamp": "2025-12-15T10:30:00.000Z",
  "version": "1.0.0"
}
```

## Deployment

This application is automatically packaged by GitHub Actions CI pipeline and deployed to Azure App Service via the CD pipeline.
