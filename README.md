# PyAction

One-stop, zero-configuration GitHub Action for linting and enforcing style in Python projects.

![Screenshot of annotations](static/annotations.png)

## Features

- Zero configuration based: Add a single line in your CI and done!
- GitHub Annotations on PR: Highlights issues inline on the PR diff.
- all of most popular community trusted linters in one place.

## Linters supported

- [black](https://github.com/psf/black)
- [flake8](http://flake8.pycqa.org)
- [isort](https://github.com/timothycrosley/isort)
- [mypy](http://mypy-lang.org/)
- [pylint](https://www.pylint.org/)
- [pycodestyle](https://pycodestyle.readthedocs.io)
- [vulture](https://github.com/jendrikseipp/vulture)

## Usage

Basic:

```yml
steps:
  - uses: actions/checkout@v1
  - uses: rahul-deepsource/pyaction@1.4.0
```

Options:

```yml
steps:
  - uses: actions/checkout@v1
  - uses: rahul-deepsource/pyaction@1.4.0
    with:
      python-root-list: "src/ tests/"
      use-pycodestyle: false
      use-mypy: false
      use-vulture: true
      extra-pylint-options: "--output-format="colorized"
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE)

## Contributions

Contributions are welcome! See [CONTRIBUTING.md](CONTRIBUTING.md)

## Thanks to

- Ricardo Baltazar Chaves' [python-lint](https://github.com/ricardochaves/python-lint) which was used as a starting point for this project.
- Florian Bruhin who provided most of the regular expressions for problem matchers.
