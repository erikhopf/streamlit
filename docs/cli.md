```eval_rst
:tocdepth: 1
```

# Command-line interface

When you install Streamlit, the Streamlit command-line CLI tool gets installed
as well. The main purpose of this tool is to help you diagnose and fix issues.

You can find docs for our CLI tool as usual:

```bash
$ streamlit --help
```

Below are a few of the most useful commands accepted by Streamlit CLI:

## Run Streamlit apps

```bash
$ streamlit run your_script.py [-- script args]
```

Runs your app. At any time you can kill the server with **Ctrl+c**.

```eval_rst
.. note::
  When passing your script some arguments, **they must be passed after a `--`**
  (double dash). Otherwise the arguments get interpreted as anything arguments
  to Streamlit itself.
```

You can also pass in config options to `streamlit run`. These allow you to do
things like change the port the app is served from, disable run-on-save, and
more. To see all options, run:

```bash
$ streamlit run --help
```

```eval_rst
.. tip::
  If you want to permanently set certain config options, just add them to
  `$CWD/.streamlit/config.toml` or to a global
  `~/.streamlit/config.toml`. More info below.
```

## Run a cool demo

```bash
$ streamlit hello
```

Opens Streamlit's Hello World app in a web browser. This is useful for
testing Streamlit.

## View all config options

```bash
$ streamlit config show
```

Shows all config options available for Streamlit, including their current
values. You can set these options in three different ways:

- **Globally:** `~/.streamlit/config.toml`.

- **Per project:** `$CWD/.streamlit/config.toml`, where `$CWD` is
  the folder you're running Streamlit from.

- **Per execution:** just pass the options as flags when running `streamlit run`. See more info above.

## Clear the cache

```bash
$ streamlit cache clear
```

Clears persisted files from the [Streamlit
cache](api.html#optimize-performance), if any.

## View documentation

```bash
$ streamlit docs
```

Opens Streamlit's documentation (i.e. this website) in a web browser.

## Print Streamlit's version

```bash
$ streamlit --version
```

Shows the version of Streamlit in your current Python environment.
