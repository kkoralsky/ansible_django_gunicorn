Django gunicorn 
===============

Run Django app through gunicorn web application server

Requirements
------------

Debian, Django


Role Variables
--------------

- `app` - determines directory structure and process names - required (handled by `django_common`);
- `program_name` - custom supervisor's config file name and process name (if empty derived from variable above)
- `gunicorn_conf_tpl` - path to `gunicorn.conf.py` template with custom configuration
- `gunicorn_unix_sock` - path to unix socket file; if specified 2 lines below are omitted
- `gunicorn_host` - default: 127.0.0.1
- `gunicorn_port` - default: 8000
- `gunicorn_loglevel` - default: `error`

Dependencies
------------

- `xkoralsky.debian_common`
- `xkoralsky.django_common`
- `xkoralsky.django_supervisor`

License
-------

BSD
