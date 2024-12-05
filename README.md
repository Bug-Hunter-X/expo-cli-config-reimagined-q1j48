# Expo CLI Configuration Error

This repository demonstrates a common error encountered when using the Expo CLI: configuration errors within `app.json` or `app.config.js`.  The error arises from typos, incorrect paths to assets, or missing dependencies.  This example shows how to identify and correct these issues.

## Error Reproduction

The `bug.js` file contains an example of an incorrectly configured `app.json` file that will trigger an error.  Run `expo start` to observe the error. 

## Solution

The `bugSolution.js` file provides the corrected `app.json` configuration. After making these changes, `expo start` should run successfully.

## Common Causes and Fixes:

* **Typos in package names:** Double-check the spelling of all package names in the `dependencies` and `devDependencies` sections of your `package.json` file, and ensure they are referenced correctly in `app.json` or `app.config.js` (e.g., `@react-native-community/masked-view`).
* **Incorrect asset paths:**  Verify that all paths to assets (images, fonts, etc.) are correct and relative to your project's root directory.  Avoid using absolute paths.
* **Missing dependencies:** Ensure that all required packages are installed using `expo install <package_name>`. 
* **Incorrect version numbers:** Ensure compatibility between your Expo SDK version and the versions of the packages you use.  Check for updates and resolve any version conflicts.
* **Syntax errors in JSON:** Validate the JSON syntax of your `app.json` or `app.config.js` using a JSON validator to catch any formatting issues like missing commas or brackets.