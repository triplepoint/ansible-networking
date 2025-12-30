# Ansible Collection - triplepoint.networking

Documentation for the collection.

## Role Testing

These roles are tested with `molecule`, using `uv` to handle dependencies and the Python testing environment.

### Setting Up Your Execution Environment

Be sure to have `uv` installed.

Once you have `uv` installed, you can build the execution virtualenv with:

```sh
uv sync --extra dev
```

### Running Tests

Once you have your environment configured, you can execute `molecule` with:

```sh
uv --directory roles/some_role run molecule test
```

### Regenerating the Lock File

You shouldn't have to do this very often, but if you change the Python package requirements using `uv add {some_package}` commands or by editing the `pyproject.toml` directly, or if you find the build dependencies have fallen out of date, you might need to regenerate the `uv.lock`.

```sh
uv lock
```

Be sure and check in the regenerated `uv.lock` when this process is complete.
