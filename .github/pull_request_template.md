## What changed
This pull request adds documentation and contribution hygiene improvements to the repository.

Changes include:
- Added a pull request template in `.github/pull_request_template.md`
- Added a personal pre-PR self-review checklist in `docs/pr-checklist.md`
- Updated `README.md` with a new **How to run** section explaining how to set up the environment, run the project, and verify success

No application logic or tests were modified.

## Why
These changes improve repository maintainability and collaboration workflow.
The PR template helps contributors provide clear and consistent information when opening pull requests.
The self-review checklist ensures contributors verify quality before submitting changes.
The How to run section helps reviewers quickly set up and execute the project locally.

## How to test
Steps to verify the changes:

1. Pull this branch locally.
2. Open the repository and confirm the following files exist:
   - `.github/pull_request_template.md`
   - `docs/pr-checklist.md`
3. Open `README.md` and verify a **How to run** section is present.
4. Confirm instructions are clear and executable.

## Checklist
Before opening this PR, I confirm that:

- [x] The code works as expected
- [x] I tested the changes locally
- [x] No debug prints or temporary code remain
- [x] Documentation is updated if needed
- [x] The PR focuses on a single logical change