app fails to run. needs fixing. 

```
2012-10-19T12:56:01-0700 app.0 stderr     return import_module('.base', backend_name)
2012-10-19T12:56:01-0700 app.0 stderr   File "/staging/staged/app/lib/python2.7/site-packages/django/utils/importlib.py", line 35, in import_module
2012-10-19T12:56:01-0700 app.0 stderr     __import__(name)
2012-10-19T12:56:01-0700 app.0 stderr   File "/staging/staged/app/lib/python2.7/site-packages/django/db/backends/postgresql_psycopg2/base.py", line 8, in <module>
2012-10-19T12:56:01-0700 app.0 stderr     from django.db import utils
2012-10-19T12:56:01-0700 app.0 stderr ImportError: cannot import name utils
```

i can run `DJANGO_SETTINGS_MODULE=syte.settings python -c "import django.db.utils"` from `s ssh` just fine.

ref - http://stackoverflow.com/questions/12112427/from-django-db-import-utils-importerror-cannot-import-name-utils

