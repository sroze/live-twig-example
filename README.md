# LiveTwig Example

This is a simple example of an application using [Live Twig](https://github.com/sroze/live-twig).

## 1. Prepare the application

1. Get Mercure Hub running. You can have a look to [the Mercure documentation](https://github.com/dunglas/mercure).
  Simplest is with Docker:
    ```
    docker run --rm -e CORS_ALLOWED_ORIGINS='http://localhost:8000' -e JWT_KEY='!ChangeMe!' -e DEMO=1 -e ALLOW_ANONYMOUS=1 -e PUBLISH_ALLOWED_ORIGINS='http://localhost,http://localhost:8000' -p 80:80 dunglas/mercure
    ```
   
2. Get your Mercure JWT token. If you are using the default demo `JWT_KEY`, you can get the token from
   [your running hub's homepage.](http://localhost/).

2. Set environment variables
    ```
    # .env
    # ...
    
    MERCURE_PUBLISH_URL=http://localhost/.well-known/mercure
    MERCURE_JWT_TOKEN=[your-token]
    ```

## 2. Run.

```
bin/console server:run
```
