# my-personal-ruby-docker-build

### Creating new ruby project
To create new ruby project, do the follow command on the CLI.

`docker run -it --rm --user "$(id -u):$(id -g)" -v "$PWD":/usr/src/app -w /usr/src/app rails rails new --skip-bundle my_app_name --database=postgresql`


### Execute bundle install after build
IN the project file do:

`docker-compose build`

`docker-compose run --rm website bundle install`

### Run docker compose
Because of the cache of gems, is necessary to use "docker-compose run --rm website bundle exec" before ruby commands. Follow the example:

`docker-compose run --rm website bundle exec rails generate rspec:install`
