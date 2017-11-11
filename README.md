# Prompt

[![Version][version-image]][github-release]
[![License][license-image]][github-license]
[![Build Status][build-image]][travis-detail]
[![Coverage][coverage-image]][coveralls-detail]

This [Ansible][ansible] module provides support to display simple messages to the user running a Playbook.  This
provides a cleaner way to present messages to the user than with the built-in [debug][ansible-debug] task.
Optionally, the message can also be treated as a prompt to await user feedback.  The response for these prompts can
be registered as Ansible variables.

## Installation

Coming Soon - Ansible Galaxy instructions.

### Manual Installation

To add this plugin to your project, simply copy the `/action_plugins/prompt.py` file to a folder named
`action_plugins` in your playbook root directory.  Ansible will automatically find and enable all commands made
available by the plugin, as detailed in the [Usage](#usage) guidelines.

### Dependencies

This module has been tested with [Ansibe][ansible] v2.0 and above.  It may work with other versions, but they are not
formally supported.  Once Ansible and it's dependencies have been installed, this plugin should be usable.

## Usage

Functionality is currently very limited for the Ansible Prompt module.  At this point, only messaging the user is
supported.

The Ansible Prompt plugin takes a single parameter, `msg`, which can contain one-or-more messages for the user.
Examples tasks are as follows:

```yaml
- name: Simple Message
  prompt:
    msg: Hello World

- name: Multiple Messages
  prompt:
    msg:
      - Hello World
      - Hello Universe
```

More functionality will be made available in future versions of this plugin.

## Contributing

There are many ways to contribute to this project!  If you have an idea, or have discovered a bug, please
[open an issue][github-issue] so it can be addressed.

If you are interested in contributing to the project through design or development, please read our
[Contribution Guidelines][github-contribute].

### Testing

A `Makefile` is provided to assist with linting, testing, and code coverage generation.  Dependencies will be managed
automatically during testing:

```bash
make test      # Runs linting and test suites
make coverage  # Runs linting, tests, and generates an HTML coverage report
```

*Please note that full tests must be provided when making contributions to this project.*

## Release Policy

Releases of this project follow [Semantic Versioning][semver] standards in a `MAJOR.MINOR.PATCH`
versioning scheme of the following format:

* `MAJOR` - modified when major, incompatible changes are made to the application,
* `MINOR` - modified when functionality is added in a backwards-compatible manner, and
* `PATCH` - patches to existing functionality, such as documentation and bug fixes.

## License

This project is made available under the [MIT License][github-license].

```
Copyright 2017 Andrew Vaughan

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit
persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the
Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```


[version-image]:     http://img.shields.io/badge/release-0.1.0-blue.svg?style=flat
[license-image]:     http://img.shields.io/badge/license-MIT-blue.svg?style=flat
[build-image]:       https://travis-ci.org/andrewvaughan/ansible-prompt.svg?branch=master
[coverage-image]:    https://coveralls.io/repos/github/andrewvaughan/ansible-prompt/badge.svg?branch=master

[github-contribute]: https://github.com/andrewvaughan/ansible-prompt/blob/master/.github/CONTRIBUTING.md
[github-issue]:      https://github.com/andrewvaughan/ansible-prompt/issues
[github-license]:    https://github.com/andrewvaughan/ansible-prompt/blob/master/LICENSE
[github-release]:    https://github.com/andrewvaughan/ansible-prompt/releases

[travis-detail]:     https://travis-ci.org/andrewvaughan/ansible-prompt
[coveralls-detail]:  https://coveralls.io/github/andrewvaughan/ansible-prompt?branch=master

[ansible]:           https://www.ansible.com/
[ansible-debug]:     http://docs.ansible.com/ansible/latest/debug_module.html
[semver]:            http://semver.org/
