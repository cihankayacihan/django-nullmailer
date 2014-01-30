django-nullmailer
=================

A django EMAIL_BACKEND for enqueuing mail in nullmailer spool system

To use just add this line to your project settings.py:

```py
EMAIL_BACKEND = 'nullmailer.backend.EmailBackend'
```

by default the class uses the /var/spool/nullmailer directory.

You can change it using the NULLMAILER_SPOOLDIR constant in settings.py

```py
NULLMAILER_SPOOLDIR = '/var/spool/foobar'
```

The module assumes your django app has write access to the nullmailer spool directory (generally the directory is owned by the 'mail' user, a good trick is giving it write access to the 'mail' group and putting the uid running the django app in the 'mail' group)
