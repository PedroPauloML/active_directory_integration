# Active Directory Integration

Configuration developed with the help of the post: https://medium.com/@takatoyo/step-by-step-implement-active-directory-auth-with-devise-33590bd3e3f1

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

### Enviroment variables

The project needs two enviroment variables: `LDAP_HOST`, `LDAP_ATTRIBUTE`, `LDAP_BASE`, `LDAP_USER` and `LDAP_USER_PASSWORD`.

To export this variables, run:

```
export LDAP_ATTRIBUTE=<value>
export LDAP_BASE=<value>
export LDAP_USER=<value>
export LDAP_HOST=<value>
export LDAP_USER_PASSWORD=<value>
```

Or add on your `~/.bash_profile`:

```
LDAP_ATTRIBUTE=<value>
LDAP_BASE=<value>
LDAP_USER=<value>
LDAP_HOST=<value>
LDAP_USER_PASSWORD=<value>
```
