# Basic, local WordPress app on Docker

This is a very basic docker compose configuration to set up a WordPress app on Docker locally. You'll get latest WordPress with Apache 2.4, PHP 5.6 and MySql 5.7.

## Getting your first WordPress app running on Docker

1. Install [Docker Community Edition](https://www.docker.com/community-edition) on your computer. Make sure you've enabled the local drive used for your project folder in Docker's Shared Drives settings.
2. Create your WordPress project directory, enter that directory and open terminal there
3. Clone this repo into that directory with `git clone https://github.com/qriouslad/basic-wordpress-docker.git .` (include a dot at the end there)
4. Run `docker compose up` and see how Docker pulls the `mysql` and `wordpress` images fron the online [Docker Hub](https://hub.docker.com/) and builds your WordPress app locally.
5. You should see all the WordPress folders created in your project folder.
6. Wait for a couple of minutes for Docker to finish initializing the containers for the database and WordPress. You should see the `wordpress` container running at the end of the `docker compose up` process in step 4.
7. Visit the WordPress app in your browser at `localhost:8000` and complete the 5-minutes install
8. Congrats. Your first, local WordPress installation in Docker. :-)

## Shutdown and clean up

`docker-compose down` will remove the containers and default network, but preserve your wordpress database. `docker-compose down --volumes` will remove the containers, default network, and the wordpress volume. It will not delete the WordPress files and folders in your project directory. If you want to start over, simply delete all the WordPress files and folders and repeat from step 3.

## References

Docker CLI documentation for:

- `docker-compose up`: https://docs.docker.com/compose/reference/up/ 
- `docker-compose down`: https://docs.docker.com/compose/reference/down/

## Sources

This simple configuration is based on [an official Docker documentation](https://docs.docker.com/compose/wordpress/#define-the-project) and [a docker tutorial by @tatemz](https://medium.com/@tatemz/local-wordpress-development-with-docker-3-easy-steps-a7c375366b9).
