# Minimal Repository for Testing Dependabot Updates with Bun

This repository is created for testing Dependabot updates using the bun package manager. It includes a `bun.lock` file and a Dependabot configuration file specifying the `npm_and_yarn` ecosystem.

## Overview

The purpose of this repository is to provide a minimal setup for testing Dependabot updates. It uses the bun package manager to manage dependencies and includes a `bun.lock` file to ensure consistent installations.

## Usage

1. Initialize the repository with a `package.json` file using `bun init`.
2. Install example dependencies using `bun add express lodash` to generate a `bun.lock` file.
3. Configure Dependabot by creating a `.github/dependabot.yml` file with the following content:
   ```yaml
   version: 2
   updates:
     - package-ecosystem: "npm"
       directory: "/"
       schedule:
         interval: "daily"
   ```

## Dependencies

- express
- lodash

## Configuration

The `.github/dependabot.yml` file is used to configure Dependabot for the `npm_and_yarn` ecosystem. Dependabot will check for updates daily and create pull requests for any available updates.
