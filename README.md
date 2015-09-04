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

Any executable file in `$DKR_HOME` will be sourced. `$DKR_HOME` by default is `~/.dkr`.

Any bash function matching the pattern: `dkr-{name}` will be added as a new function of dkr and can be called with `dkr {name}`.

The summarys are chosen by any function named `dkr-{name}-summary_`
