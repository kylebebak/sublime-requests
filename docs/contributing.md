# Contributing
Please do! Possible improvements:

- Better test coverage
  + Tests for error messages
  + Tests for proper parsing of env block and env files
  + Tests for activity indicators
- Create a testing framework that allows users to make assertions about responses for given requests
  + Perform test runs
  + View results
- Import from and export to common request formats (HTTP, cURL, etc)
  + Import collection from Postman?


## Python Code Style
Try to limit lines to 100 characters or less, unless doing so is inconvenient. No lines with more than 120 characters.

Two lines between classes or top-level methods. One line between class methods. Within methods, use vertical whitespace if it improves readability, but never more than one line.

Indentation: 4 spaces. No tabs.

All classes and methods should have docstrings, limited to 82 characters per line. Except for `run` methods. Feel free to add comments for anything that's not obvious.


## Tests
Install __UnitTesting__ via Package Control. Read more about [UnitTesting](https://github.com/randy3k/UnitTesting-example). Also, make sure you've cloned the Requester repo into your __Packages__ directory.

Run tests before committing changes. Look for __UnitTesting__ in the command palette, hit enter, and enter `Requester`. Or, if you've created a project for Requester, run __UnitTesting: Test Current Project__.

Many tests for Requester are asynchronous, because they depend on responses coming back before examining response tabs. This means tests may fail simply because a response wasn't returned on time. This is a false positive, just run the tests again.

This is also why I'm reluctant to use something like Travis, because the build may fail even when nothing is wrong with the package.