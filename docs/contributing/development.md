# Development

React Async is a library without visual parts. Only the DevTools have a user interface you can spin up in a browser.
Therefore the development workflow for the core library might be different from what you're used to. Generally, we use a
TDD approach:

- Write a unit test for the new feature or bug you want to fix. Sometimes you can just extend an existing test.
- Fix the test by implementing the feature or bugfix. Now all tests should pass.
- Optionally refactor the code for performance, readability and style. Probably this will come up during PR review.

We use the GitHub pull request workflow. In practice this means your workflow looks like this:

- Fork the repo (or pull the latest upstream) under your own account.
- Make your changes, commit and push them. We don't enforce any commit message format.
- Open a pull request on the main repository against the `next` branch. Make sure to follow the template.
- We'll review your PR and will probably ask for some changes.
- Once ready, we'll merge your PR.
- Your changes will be in the next release.

## Working with Storybook

We use Storybook as a development environment for the DevTools. Spin it up using:

```sh
yarn start:storybook
```

This should open up Storybook in a browser at http://localhost:6006/
Run it side-by-side with `yarn test --watch` during development. See [Testing](#testing).
