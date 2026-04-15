# FullStack-internship

A full-stack internship project. This repository serves as a hands-on learning environment for building and contributing to a full-stack web application.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Interactive Tutorial](#interactive-tutorial)
  - [Step 1: Fork and Clone the Repository](#step-1-fork-and-clone-the-repository)
  - [Step 2: Explore the Project Structure](#step-2-explore-the-project-structure)
  - [Step 3: Install Dependencies](#step-3-install-dependencies)
  - [Step 4: Set Up Environment Variables](#step-4-set-up-environment-variables)
  - [Step 5: Run the Application](#step-5-run-the-application)
  - [Step 6: Run the Tests](#step-6-run-the-tests)
  - [Step 7: Make Your First Change](#step-7-make-your-first-change)
  - [Step 8: Commit and Push Your Change](#step-8-commit-and-push-your-change)
  - [Step 9: Open a Pull Request](#step-9-open-a-pull-request)
- [Troubleshooting](#troubleshooting)
- [License](#license)

---

## Prerequisites

Before starting, make sure you have the following installed on your machine:

| Tool | Minimum Version | Installation Guide |
|------|----------------|--------------------|
| [Git](https://git-scm.com/) | 2.30+ | [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) |
| [Node.js](https://nodejs.org/) | 18+ | [Install Node.js](https://nodejs.org/en/download/) |
| [npm](https://www.npmjs.com/) | 9+ | Included with Node.js |

> **Verify your setup** by running the following commands in your terminal:
> ```bash
> git --version
> node --version
> npm --version
> ```
> Each command should print a version number. If any command is not found, follow the installation guide linked above.

---

## Interactive Tutorial

Welcome! This step-by-step tutorial will walk you through setting up the project, running the tests, and making your first contribution. Each step includes checkboxes so you can track your progress.

### Step 1: Fork and Clone the Repository

- [ ] **Fork** this repository by clicking the **Fork** button at the top-right corner of this page on GitHub.

- [ ] **Clone** your forked repository to your local machine:

  ```bash
  git clone https://github.com/<your-username>/FullStack-internship.git
  ```

  > Replace `<your-username>` with your GitHub username.

- [ ] **Navigate** into the project directory:

  ```bash
  cd FullStack-internship
  ```

- [ ] **Add the upstream remote** so you can pull future updates from the original repository:

  ```bash
  git remote add upstream https://github.com/sushmitakundarnad/FullStack-internship.git
  ```

- [ ] **Verify** your remotes are set up correctly:

  ```bash
  git remote -v
  ```

  You should see both `origin` (your fork) and `upstream` (the original repo).

<details>
<summary><strong>What did I just do?</strong> (click to expand)</summary>

You created a personal copy (fork) of the project on GitHub, downloaded it to your computer, and linked it back to the original repository. This is the standard open-source contribution workflow.
</details>

---

### Step 2: Explore the Project Structure

- [ ] Take a moment to look at the files and folders in the repository:

  ```bash
  ls -la
  ```

  Here is an overview of the key files:

  ```
  FullStack-internship/
  ├── README.md          # This file - project documentation and tutorial
  ├── LICENSE            # Apache 2.0 license
  ├── src/               # Application source code (coming soon)
  │   ├── index.js       # Main entry point
  │   └── utils.js       # Utility/helper functions
  ├── tests/             # Test files (coming soon)
  │   └── utils.test.js  # Tests for utility functions
  └── package.json       # Node.js project configuration and dependencies
  ```

  > **Note:** As this project evolves, new folders and files will be added. Always check the latest structure after pulling updates.

<details>
<summary><strong>Why does structure matter?</strong> (click to expand)</summary>

Understanding the project layout helps you know where to find things and where to add new code. In most full-stack projects, you will see separate directories for source code (`src/`), tests (`tests/`), configuration files, and documentation.
</details>

---

### Step 3: Install Dependencies

- [ ] **Install** the project dependencies using npm:

  ```bash
  npm install
  ```

  This reads the `package.json` file and downloads all required packages into a `node_modules/` folder.

- [ ] **Verify** the installation completed without errors. You should see output similar to:

  ```
  added XX packages in Xs
  ```

<details>
<summary><strong>What is <code>package.json</code>?</strong> (click to expand)</summary>

`package.json` is the manifest file for Node.js projects. It lists the project's dependencies (libraries it needs), scripts (commands you can run), and metadata (name, version, description). Think of it as the project's "recipe card."
</details>

---

### Step 4: Set Up Environment Variables

- [ ] **Copy** the example environment file (if one exists):

  ```bash
  cp .env.example .env 2>/dev/null || echo "No .env.example found - skipping"
  ```

- [ ] **Edit** the `.env` file (if created) and fill in any required values. Open it with your preferred editor:

  ```bash
  # Using VS Code
  code .env

  # Or using nano
  nano .env
  ```

  > **Tip:** Never commit `.env` files to version control. They often contain secrets and API keys. The `.gitignore` file should already exclude them.

<details>
<summary><strong>Why use environment variables?</strong> (click to expand)</summary>

Environment variables let you configure the application differently for development, testing, and production without changing the code. For example, you might use a local database URL in development and a cloud database URL in production.
</details>

---

### Step 5: Run the Application

- [ ] **Start** the development server:

  ```bash
  npm start
  ```

  > If a `start` script is not yet configured, you can run the main file directly:
  > ```bash
  > node src/index.js
  > ```

- [ ] **Open your browser** and navigate to the URL shown in the terminal (typically `http://localhost:3000`).

- [ ] **Confirm** you can see the application running. You should see a welcome page or API response.

  > **Tip:** Press `Ctrl + C` in the terminal to stop the server when you are done.

<details>
<summary><strong>What happens when I run <code>npm start</code>?</strong> (click to expand)</summary>

The `npm start` command looks for a `"start"` script in `package.json` and executes it. This typically launches a local development server that watches your files for changes and automatically reloads the application.
</details>

---

### Step 6: Run the Tests

- [ ] **Run** the test suite to make sure everything passes:

  ```bash
  npm test
  ```

- [ ] **Review** the test output. You should see results like:

  ```
  PASS  tests/utils.test.js
    ✓ should return the correct value (5 ms)

  Test Suites: 1 passed, 1 total
  Tests:       1 passed, 1 total
  ```

- [ ] If any tests fail, read the error messages carefully. They will tell you which test failed and why.

<details>
<summary><strong>Why run tests first?</strong> (click to expand)</summary>

Running the tests before making any changes establishes a **baseline**. If all tests pass now, and a test fails after your change, you know your change caused the failure. This is a fundamental practice in software development called **regression testing**.
</details>

---

### Step 7: Make Your First Change

Now that everything is set up and the tests pass, let's make a simple change to practice the contribution workflow.

#### 7a. Create a New Branch

- [ ] Always create a new branch for your changes - never work directly on `main`:

  ```bash
  git checkout -b feature/add-greeting
  ```

#### 7b. Make a Code Change

- [ ] Open `src/utils.js` (or create it if it does not exist) and add a new function:

  ```javascript
  /**
   * Returns a personalized greeting message.
   * @param {string} name - The name of the person to greet.
   * @returns {string} A greeting message.
   */
  function greet(name) {
    return `Hello, ${name}! Welcome to the FullStack Internship!`;
  }

  module.exports = { greet };
  ```

#### 7c. Write a Test for Your Change

- [ ] Open `tests/utils.test.js` (or create it if it does not exist) and add a test:

  ```javascript
  const { greet } = require('../src/utils');

  describe('greet', () => {
    test('should return a greeting with the provided name', () => {
      const result = greet('Alice');
      expect(result).toBe('Hello, Alice! Welcome to the FullStack Internship!');
    });

    test('should include the name in the greeting', () => {
      const result = greet('Bob');
      expect(result).toContain('Bob');
    });
  });
  ```

#### 7d. Run the Tests Again

- [ ] Verify that your new test passes alongside all existing tests:

  ```bash
  npm test
  ```

  You should see your new tests in the output:

  ```
  PASS  tests/utils.test.js
    greet
      ✓ should return a greeting with the provided name (3 ms)
      ✓ should include the name in the greeting (1 ms)
  ```

<details>
<summary><strong>Why write tests for every change?</strong> (click to expand)</summary>

Tests serve as living documentation and a safety net. They describe what your code is supposed to do and alert you when something breaks. In professional development, most teams require tests for all new code before it can be merged.
</details>

---

### Step 8: Commit and Push Your Change

- [ ] **Stage** your changes:

  ```bash
  git add src/utils.js tests/utils.test.js
  ```

  > **Tip:** Use `git status` to see which files have been modified and `git diff` to review your changes before staging.

- [ ] **Commit** with a descriptive message following conventional commit format:

  ```bash
  git commit -m "feat: add greet function with tests"
  ```

  > **Conventional commit prefixes:**
  > - `feat:` - A new feature
  > - `fix:` - A bug fix
  > - `docs:` - Documentation changes
  > - `test:` - Adding or updating tests
  > - `refactor:` - Code restructuring without changing behavior

- [ ] **Push** your branch to your fork:

  ```bash
  git push origin feature/add-greeting
  ```

<details>
<summary><strong>What is a conventional commit?</strong> (click to expand)</summary>

Conventional commits are a standardized format for commit messages. They make the project history easier to read, enable automated changelog generation, and help team members understand the purpose of each change at a glance.
</details>

---

### Step 9: Open a Pull Request

- [ ] Go to your fork on GitHub. You should see a banner suggesting you create a pull request.

- [ ] Click **"Compare & pull request"**.

- [ ] Fill in the PR template:
  - **Title:** A concise summary (e.g., "Add greet function with tests")
  - **Description:** Explain what you changed and why. Reference any related issues.

- [ ] Click **"Create pull request"**.

- [ ] Wait for any CI checks to pass, then request a review from a maintainer.

**Congratulations!** You have just completed the full contribution workflow:
1. Forked and cloned the repo
2. Set up the development environment
3. Ran the existing tests
4. Created a feature branch
5. Made a code change with tests
6. Committed, pushed, and opened a PR

---

## Troubleshooting

<details>
<summary><strong><code>npm install</code> fails with permission errors</strong></summary>

Try running:
```bash
npm install --legacy-peer-deps
```

If that does not work, ensure you have the correct version of Node.js installed (v18+).
</details>

<details>
<summary><strong><code>npm test</code> says "no test specified"</strong></summary>

Make sure the `"test"` script in `package.json` is configured correctly. It should point to your test runner, for example:
```json
{
  "scripts": {
    "test": "jest"
  }
}
```
</details>

<details>
<summary><strong><code>git push</code> is rejected</strong></summary>

This usually means the remote branch has changes you do not have locally. Pull the latest changes first:
```bash
git pull origin main --rebase
```
Then try pushing again.
</details>

<details>
<summary><strong>Port already in use</strong></summary>

If you see `EADDRINUSE`, another process is using the port. Find and stop it:
```bash
# Find the process using port 3000
lsof -i :3000

# Kill it (replace <PID> with the actual process ID)
kill -9 <PID>
```
</details>

---

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.