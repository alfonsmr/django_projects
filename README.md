# django_projects

edit the WGSI Configuration File 

```python
import os
import sys

path = os.path.expanduser('~/django_projects/mysite')
if path not in sys.path:
    sys.path.insert(0, path)
os.environ['DJANGO_SETTINGS_MODULE'] = 'mysite.settings'
from django.core.wsgi import get_wsgi_application
from django.contrib.staticfiles.handlers import StaticFilesHandler
application = StaticFilesHandler(get_wsgi_application())
```
Cómo trabajar con git branches

Trabajaremos en la rama Development, haciendo nuevas ramas a partir de esta para cada tarea
Una vez entregada y funcionando la tarea se hace un merge a Development
depues se hace merge a master

Listar ramas de git para el proyecto disponibles
git branch

Queremos crear una nueva rama desde "development" por lo que nos movemos a development
git checkout development

Creamos la rama a partir de development con el nombre que queramos, p.e. "feature_branch"
git checkout -b feature_branch development

Conectamos la rama local al servidor remoto
git push --set-upstream origin feature_branch
