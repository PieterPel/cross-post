# Battle Plan: Upgrade Node.js from v14 to v22

This document outlines the steps to upgrade the Node.js version for the cross-post project from v14 to v22.

## 1. Initial Setup

*   [ ] **Install Node.js v22:** Ensure Node.js v22 is installed on the development machine. I recommend using a version manager like `nvm` to easily switch between Node.js versions.
    ```bash
    nvm install 22
    nvm use 22
    ```
*   [ ] **Verify Node.js and npm versions:**
    ```bash
    node -v
    npm -v
    ```

## 2. Dependency Update

*   [ ] **Delete `node_modules` and `package-lock.json`:** This will ensure a clean installation of dependencies.
    ```bash
    rm -rf node_modules package-lock.json
    ```
*   [ ] **Update `npm`:**
    ```bash
    npm install -g npm@latest
    ```
*   [ ] **Run `npm install`:**
    ```bash
    npm install
    ```

## 3. Testing

*   [ ] **Run the application:**
    ```bash
    npm start
    ```
*   [ ] **Test all commands:**
    *   [ ] `run`
    *   [ ] `config cloudinary`
    *   [ ] `config dev`
    *   [ ] `config hashnode`
    *   [ ] `config imageSelector`
    *   [ ] `config medium`
    *   [ ] `config reset`
    *   [ ] `config selector`
    *   [ ] `config titleSelector`
    *   [ ] `reset all`
    *   [ ] `reset cloudinary`
    *   [ ] `reset dev`
    *   [ ] `reset hashnode`
    *   [ ] `reset medium`

## 4. Code Refactoring (if necessary)

*   [ ] **Address any breaking changes:** If any of the dependencies have breaking changes, update the code accordingly.
*   [ ] **Update `.github/workflows`:** If there are any GitHub Actions workflows, update them to use Node.js v22.

## 5. Final Steps

*   [ ] **Update `package.json`:** Update the `engines` section in `package.json` to reflect the new Node.js version.
    ```json
    "engines": {
      "node": ">=22.0.0"
    }
    ```
*   [ ] **Update documentation:** Update the `README.md` file to reflect the new Node.js version requirement.
*   [ ] **Commit changes:**
    ```bash
    git add .
    git commit -m "feat: upgrade Node.js to v22"
    ```
