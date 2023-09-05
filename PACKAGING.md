# Packaging

The following are requirements for a working installation of Hyprshade:

- Python 3.11+
- Dependencies: see `pyproject.toml`'s `project.dependencies`
- Build dependencies: [Hatchling](https://hatch.pypa.io/latest/) (not required
  if you install from wheel)

The following are also recommended:

- Using [`python-build`](https://pypa-build.readthedocs.io/en/stable/) and
  [`python-installer`](https://installer.pypa.io/en/stable/) for building and
  installation respectively
  - When building from PyPI's source distribution, download `examples/` and `shaders/`
    to make sure they are included in the wheel file's [`.data` directory](https://packaging.python.org/en/latest/specifications/binary-distribution-format/#the-data-directory);
    they will automatically be installed to `/usr/share/hyprshade/` by `python-installer`
    (this is not necessary if you install from PyPI's wheel distribution)
- `LICENSE` file (destination: `/usr/share/licenses/hyprshade/`)
- Completions (see [Click documentation](https://click.palletsprojects.com/en/8.1.x/shell-completion/)
  for how to generate them)

See [the Arch Linux PKGBUILD](https://github.com/loqusion/aur-packages/blob/master/hyprshade/PKGBUILD)
for reference.