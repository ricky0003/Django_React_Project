# docker-django-react

## Main Frameworks/Libraries/Packages

Please see requirements.txt and package.json for full details.

Django

- Django v5
- Django Rest Framework
- Django Rest Framework Simple JWT
- PyTest

React

- Create React App
- Node dev server via Docker LTS alpine image
- Hot reload

Postgress

- Docker v16.1 alpine image

Ngnix

- Docker stable alpine
- Serves Django's static and media files as well.  See conf for details.

## Notes

Django

- One app created/installed called core
- Custom user stubbed out in the Core app. No additional fields. Just a blank class that inherets AbstractUser. core.User is assigned as AUTH_USER_MODEL
- SimpleJWT is installed but not used.


### Useful Commands

Build containers. Add -up flag to bring services up after build.

```sh

$> docker compose build

```

Bring containers up. Add -d flag to run output detached from current shell.

```sh

$> docker compose up

```

Bring containers down. Add -v flag to also delete named volumes

```sh

$> docker compose down

```

View logs by service name.

```sh

$> docker compose logs <service-name>

```

Enter shell for specified container (must be running)

```sh

$> docker exec -it <container-name> sh

```


