# my-personal-ruby-docker-build

### Execute bundle install after build
IN the project file do:
`docker-compose build`
`docker-compose run --rm website bundle install`

### Run docker compose
Because of the cache of gems, is necessary to use "docker-compose run --rm website bundle exec" before ruby commands. Follow the example:
`docker-compose run --rm website bundle exec rails generate rspec:install`
