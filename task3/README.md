# Task 3: Node.js Hello Xops

This project is a simple Node.js application that responds with "Hello, welcome to Xops" on the root route (`/`).

# Scrrenshots

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/0b4b4370-2189-4ea3-858e-2f4e1762c7a3" />


## How to Run Locally

1. Install Node.js (https://nodejs.org/)
2. Navigate to the `task3` directory:
   ```powershell
   cd task3
   ```
3. Install dependencies:
   ```powershell
   npm install
   ```
4. Start the server:
   ```powershell
   npm start
   ```
5. Open your browser and go to `http://localhost:3000` to see the message.

## CI/CD Setup

A sample GitHub Actions workflow is provided in `.github/workflows/nodejs.yml` to automate build and test on every push.

## Files
- `app.js`: Main application file
- `package.json`: Project metadata and dependencies
- `.github/workflows/nodejs.yml`: CI/CD workflow

## Output
The root route (`/`) will display:
```
Hello, welcome to Xops
```
