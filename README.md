# CI/CD Pipeline

This project uses GitHub Actions for Continuous Integration and Continuous Delivery.

## Workflow

1. Checkout source code
2. Install dependencies using npm ci
3. Run npm audit security check
4. Execute ESLint
5. Run Vitest unit tests
6. Generate coverage report
7. Validate coverage threshold
8. Build application
9. Validate deployable artifact
10. Publish artifact

## Local Setup

Install dependencies:

npm ci

Run linting:

npm run lint

Run tests:

npm run test

Generate coverage:

npm run coverage

Build project:

npm run build

## Troubleshooting

### npm ci fails

Delete:

node_modules

package-lock.json

Reinstall:

npm install

### ESLint failures

Run:

npm run lint

Fix reported issues.

### Coverage threshold failures

Add more unit tests until:
- Lines >= 80%
- Statements >= 80%
- Functions >= 80%
- Branches >= 80%

### Build failures

Verify:
- package.json scripts exist
- vite.config.js present
- dependencies installed