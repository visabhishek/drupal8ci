# Drupal 8 CI

This repository provides the foundation to implement [Continutous Integration](https://en.wikipedia.org/wiki/Continuous_integration) in a Drupal 8
project using [CircleCI](https://circleci.com/).

It contains:

- A custom demo module with a [unit and a kernel test](web/modules/custom/demo_module/tests/src).
- A demo [Behat test](tests).
- A CircleCI workflow that when code is pushed to GitHub:
    * Runs unit tests.
    * Runs kernel tests.
    * Runs Behat tests.
    * Checks Drupal coding standards in custom modules.

If you want to test and individul module and not a whole Drupal site, see
[drupal_tests](https://github.com/deviantintegral/drupal_tests).

## Requirements

The scripts assume that your site was installed using [Composer Drupal Project](https://github.com/drupal-composer/drupal-project)
which sets a well known foundation for Drupal 8 projects. If your project's directory
structure differs from what Composer Drupal Project sets up, you will need to
adjust the CircleCI scripts so they can run successfully.

## Installation

1. Make sure that you don't have changes pending to commit in your local environment.
2. Open a terminal and run the installer from the root of your project:
```bash
curl -L https://github.com/juampynr/drupal8ci/raw/master/setup.sh | bash
```
2. Sign up at CircleCI and allow access to your project.
3. Create a branch, commit your changes and create a pull request.
4. Wait for CircleCI to add a status message at the pull request.
5. Happy CI-ing! :-D