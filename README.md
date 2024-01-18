## Sense HAT

A stripped down implementation of the Python Sense HAT package that works with
Pyodide.

This implementation is used in Raspberry Pi's
[Mission Zero](https://missions.astro-pi.org/mz/code_submissions/new)
code editor. If you are using Python on the command-line, you probably want
to use the official [python-sense-hat](https://github.com/astro-pi/python-sense-hat)
package instead.

## Demo

Run `./bin/server` then visit http://localhost:8000/demo-pyodide.html to see a
demo of the sense_hat package. The program's output is shown underneath the
textarea. The sense_hat configuration is shown in the top-right of the page.
Errors are logged to the JavaScript console. The configuration is used to update
the simulator's state.

## Limitations

This package is a heavily modified version of
[python-sense-hat](https://github.com/astro-pi/python-sense-hat) and many of
the methods raise a NotImplementedError. This package will not work with a
physical Sense HAT, only
[the simulator](https://missions.astro-pi.org/mz/code_submissions/new).

## Code History

1. The code originates from the [python-sense-hat](https://github.com/astro-pi/python-sense-hat) package.
2. It was then modified to work with [Skulpt](https://skulpt.org/) in the
editor-ui project's [shims/](https://github.com/RaspberryPiFoundation/editor-ui/tree/6f20db3cf725cb6bd6be806a96e8cb6f810092a1/public/shims/sense_hat) directory.
3. It was then modified to work with Pyodide in the
[python-execution-prototypes](https://github.com/RaspberryPiFoundation/python-execution-prototypes/compare/ba1ae9e1...61c25ec) project.
