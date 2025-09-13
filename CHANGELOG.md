## [0.8.0]
    - Better evaluate version of main branch

## [0.7.0]
    - Add input working-directory in every composite

## [0.6.0]
    - Run correctly the npm type-check

## [0.5.0]
    - Rename nodejs actions to npm actions
    - Simplify build action
    - Add lint and type-check actions
    - Add --if-present where needed

## [0.4.0]
    - Add shell specification in nodejs actions

## [0.3.0]
    - Remove setup actions

## [0.2.0]
    - Update README.md
    
## [0.1.0]
    - Detect Direct Push Action & Workflow: Added an action and workflow to detect direct pushes to the `main` branch and check if the push is from a pull request merge or a direct commit.
  
    - Validate Version and Changelog Action & Workflow: Introduced an action and workflow to ensure that `VERSION` and `CHANGELOG.md` files are updated in pull requests before merging to `main`.

    - Python Actions:
        - Linting Action: Added action for linting Python code.
        - Run Tests Action: Added action to run Python tests.
        - Setup Python Action: Introduced action to set up Python environment with specified version.
        - Install Dependencies Action: Added action to install Python dependencies using `pip` from the `requirements.txt` file.

    - Node.js Actions:
        - Setup Node.js Action: Added action to set up the specified version of Node.js.
        - Install Dependencies Action: Created action to install Node.js dependencies using `npm ci`.
        - Run Tests Action: Added action to run tests with `npm test`.
        - Build App Action: Introduced action to clean npm cache, install Node.js dependencies, and run `npm run build`.