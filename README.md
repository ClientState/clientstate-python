clientstate-python
==================

Python client for ClientState API

(THIS CLIENT IS CURRENTLY VAPORWARE)

Install
-------

Install with `pip install clientstate-python` or `setup.py install`.

Setup
-----

Make an app on Github and input the credentials into a
[clientstate-master](https://github.com/ClientState/clientstate-master)
instance.

Usage
-----

Instantiate:

    HOST = "clienstate.local"
    # HOST is optional, default is clientstate.io
    cs = Clientstate(GITHUB_CLIENT_ID, GITHUB_CLIENT_SECRET, HOST)

Now you can make calls to the DB:

    cs.post("SET", "foobar", "baz")
    value = cs.get("GET", "foobar")
    assert value == "baz"

Use the `post` method to write data and the `get` method to retrieve data.
Redis commands are available and can be referenced here: http://redis.io/commands
