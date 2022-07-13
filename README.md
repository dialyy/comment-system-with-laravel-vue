# Comment System

## Requirements

-   php >= 7.3
-   nodejs = v16.8.0
-   npm = 7.21.0

The js requirements were my machine's version at the time of developing. It may work on lower versions too.

## Installation

-   ```bash
    docker exec -it alloware-app composer install && php artisan key:generate
    ```
-   do not forget to do the db setup inside the db container

-   Ps: I have node installed on my machine not inside docker

-   ```bash
    npm i && npm run prod
    ```

## Testing

For the first time you need to generate an app key for test env

```bash
docker exec -it alloware-app  php artisan key:generate --env=testing
```

and then set your configs in `.env.testing` file.

```bash
docker exec -it alloware-app  php artisan test
```
