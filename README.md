Extendable `docker` cli wrapper. Allows the user to easily add new functionality.

Any command that doesn't exist in `dkr` automatically gets delegated to `docker`.

# Install

```bash
git clone git@github.com:JoelJ/dkr.git
cd dkr
./install
```

# Usage

If you run only `dkr` help will be printed out, including a list of all the extensions. 

# Extending

Any non-executable file in `$DKR_HOME` will be sourced. `$DKR_HOME` by default is `~/.dkr`.

How commands are called:

* Any bash function matching the pattern: `dkr-{name}` will be added as a new function of dkr and can be called with `dkr {name}`.
* `$DKR_HOME` is added to the `PATH` so any executable files in `$DKR_HOME` matching the naming conventions will also be included.
* If `dkr {name}` is called and `dkr-name` does not exist, then `docker {name}` will be called instead.
* The `summarys` are chosen by any function/executable named `dkr-{name}-summary_`
* The `helps` are chosen by any function/executable named `dkr-{name}-help_`
