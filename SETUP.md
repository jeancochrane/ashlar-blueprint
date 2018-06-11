# Setup

Documenting the steps it took to set up a working Ashlar server.

- `pip install pip==9.0.1`
- `pip install --process-dependency-links -e git+https://github.com/jeancochrane/ashlar.git@update-dependencies#egg=ashlar`
- `pip install docker-compose==1.21.2`
- Initialize a Django app
- Update the settings file:
    - Define `ASHLAR` global var, set `SRID = 4326`
    - Set `DEVELOP = True`
    - In `INSTALLED_APPS`, add:

```
    'rest_framework',
    'rest_framework.authtoken',
    'django_extensions',
    'ashlar',
```
    
- Set `urlpatterns = ashlar.urls.urlpatterns` in `urls.py`
- Set up a database with PostGIS
- Run database migrations
- Run the server
