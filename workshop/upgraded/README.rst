of them are missing.
treat it like a regular dictionary!
in our twitter app by calling it this way::
has none?
it in some sub-module::

Guachi
======

**Guachi** is a modern, persistent configuration manager for Python 3.9+ projects.
It stores configuration as dictionaries, supports INI-style keys, and fills in default values as needed.

**Key Features:**
- Python 3.9+ compatible
- Modern packaging with `pyproject.toml`
- No legacy `distribute` or Python 2-only tools
- Persistent storage using SQLite
- Easy mapping from INI files to dictionary keys
- Fully tested with pytest

Quick Example
-------------

Suppose you have an INI file:

    [DEFAULT]
    app.twitter.username = alfredodeza
    app.update.frequency = 60
    app.load.startup = False

You can load and use it like this:

    conf = ConfigMapper(config_db_path)
    conf.set_config('/path/to/twitter.ini')
    db_conf = conf.stored_config()
    print(db_conf['frequency'])  # 60

If the user has no config, defaults are filled in automatically.

Updating Values
---------------

    conf = ConfigMapper(config_db_path)
    conf.update_config('/path/to/twitter.ini')

Project Status
--------------
- Python 3.9+ required
- Modern packaging: see `pyproject.toml`
- To run tests: `pytest`

For full API documentation, see the `docs/` folder.
