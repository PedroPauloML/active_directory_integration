# Active Directory Integration

## Prerequisites

- Ruby 2.6.6
- Rails 5.2.4.2
- Docker 19.03.8

## Getting started

### Run the project

To run the project, access the folder `/rails_app` and run:

```
$ bundle install
$ rails db:create db:migrate
$ rails s
```

And access, on your browser: `http://localhost:3000`.

### Run the container

To run the project with Docker, on root folder, run the follwing:

```
$ docker-compose run app bundle exec rails assets:precompile RAILS_ENV=production
$ docker-compose run app bundle exec rails db:create db:migrate RAILS_ENV=production
$ docker-compose build
$ docker-compose up -d
```

And access, on your browser: `http://localhost:8081`.

### Enviroment variables

The project needs two enviroment variables: `LDAP_HOST` and `LDAP_ADMIN_PASSWORD`.

To export this variables, run:

```
export LDAP_HOST=<value>
export LDAP_ADMIN_PASSWORD=<value>
```

Or add on your `~/.bash_profile`:

```
LDAP_HOST=<value>
LDAP_ADMIN_PASSWORD=<value>
```
