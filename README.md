# Basic, local WordPress app on Docker

This is a very basic docker compose configuration to set up a WordPress app on Docker locally. You'll get latest WordPress with Apache 2.4, PHP 5.6 and MySql 5.7.

## Getting your first WordPress app running on Docker

1. Install [Docker Community Edition](https://www.docker.com/community-edition) on your computer.
2. Create your WordPress project directory, enter that directory and open terminal there
3. Clone this repo into that directory with `git clone https://github.com/qriouslad/basic-wordpress-docker.git .` (include a dot at the end there)
4. Run `docker compose up -d`
5. You should see `database` directory in your project folder, and then all the WordPress folders created there as well
6. Wait for a couple of minutes for Docker to finish initializing the containers for the database and WordPress.
7. Visit the WordPress app in your browser at `localhost:8000` and complete the 5-minutes install
8. Congrats. Your first, local WordPress installation in Docker. :-)

## Shutdown and clean up

`docker-compose down` will remove the containers and default network, but preserve your wordpress database. `docker-compose down --volumes` will remove the containers, default network, and the wordpress database.

### Sources

This simple configuration is based on [an official Docker documentation](https://docs.docker.com/compose/wordpress/#define-the-project) and [a docker tutorial by @tatemz](https://medium.com/@tatemz/local-wordpress-development-with-docker-3-easy-steps-a7c375366b9).
