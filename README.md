<p align="center">  
The <a href="https://pypi.org/project/distributed/">distributed</a> parallel computing library hooks for xonsh
<br><br>
If you like the idea click ⭐ on the repo and <a href="https://twitter.com/intent/tweet?text=Nice%20xontrib%20for%20the%20xonsh%20shell!&url=https://github.com/xonsh/xontrib-distributed" target="_blank">tweet</a>.
</p>


Importantly this provides a substitute 'dworker' command
which enables distributed workers to have access to xonsh builtins.

Furthermore, this xontrib adds a 'DSubmitter' context manager
for executing a block remotely.
Moreover, this also adds a convenience function 'dsubmit()'
for creating DSubmitter and Executor instances at the same time.

Thus users may submit distributed jobs with::

```pycon
with dsubmit('127.0.0.1:8786', rtn='x') as dsub:
    x = $(echo I am elsewhere)
res = dsub.future.result()
print(res)
```

This is useful for long running or non-blocking jobs.

## Installation

To install use pip:

```bash
xpip install xontrib-distributed
# or: xpip install -U git+https://github.com/xonsh/xontrib-distributed
```

## Usage

```bash
xontrib load distributed
# TODO: what's next?
```

## Releasing your package

- Bump the version of your package.
- Create a GitHub release (The release notes are automatically generated as a draft release after each push).
- And publish with `poetry publish --build` or `twine`

## Credits

This package was created with [xontrib cookiecutter template](https://github.com/xonsh/xontrib-cookiecutter).

