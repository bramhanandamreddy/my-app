## Test Automation - Initial Setup process for Cypress and Cucumber

## Purpose of Cypress Tests

Cypress E2E testing ensures that the application flow operates as expected by testing the entire software product from end to end. It specifies the product’s system dependencies and guarantees that all integrated components function correctly. In this repository we are writing the Cypress tests for the API endpoints.

## Installation

Follow these steps to install and set up the Cloud Device Updater Services package on your system:

### Prerequisites

- [NVM](https://github.com/nvm-sh/nvm#installing-and-updating) recommended for managing node version if you are working with another repository.
- [Yarn](https://classic.yarnpkg.com/lang/en/docs/cli/install/) (recommended)

### Steps

- Clone the repository from GitHub:

  ```bash
  git clone https://github.com/tandemdiabetes/web-tdu-bff

  ```

- Change your current working directory to the project folder:
  ```sh
  cd web-tdu-bff
  ```
- Change the directory to the folder "e2e":
  ```sh
  cd e2e
  ```
- Install the project dependencies using Yarn:
  ```sh
  yarn install
  ```
- Run ESLint to lint the project:
  ```sh
  yarn lint
  ```
  You can also automatically fix linting issues using:
  ```sh
  yarn lint:fix
  ```

## Add environment file

- **Locate your Cypress project directory:** Make sure you are in the root directory of your Cypress project where your cypress.env.example are located.

- **Create a copy of cypress.env.example file:** If you don't already have a cypress.env.json file, you can start by copying your example file. Make sure to update the values based on your specific environment and requirements.

- **Save the changes:** After updating the environment variables in cypress.env.json, save the file.

Now your Cypress project is configured to use the custom environment variables specified in cypress.env.json during test execution. Cypress will automatically load these environment variables for your tests.

## Running cypress tests

- To run Cypress tests , open the Cypress Test Runner:

  ```sh
  yarn cy:open
  ```

- To run Cypress tests in headless mode:

  ```sh
  yarn cy:run
  ```

- You can run tests in specific environments using the following commands:

  - Local Environment: (If you want to run it locally then you need to setup mTDU backend project and run the project locally.)

    ```sh
    yarn run cy:open:local
    ```

    ```sh
    #Headless mode
    yarn run cy:run:local
    ```

  - Development Environment:

    ```sh
    yarn cy:open:dev
    ```

    ```sh
    # Headless mode
    yarn run cy:run:dev
    ```
