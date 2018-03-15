# crystal-api

This project is powered by [Amber Framework](https://amberframework.org/).

## Installation

1. [Install required dependencies](https://github.com/amberframework/online-docs/blob/master/getting-started/quickstart/zero-to-deploy.md#install-crystal-and-amber)
2. Run `shards install`

## Usage

To setup your database edit `database_url` inside `config/environments/development.yml` file.

To edit your production settings use `amber encrypt`. [See encrypt command guide](https://github.com/amberframework/online-docs/blob/master/getting-started/cli/encrypt.md#encrypt-command)

To run amber server in a **development** enviroment:

```
amber db create migrate
amber watch
```

To build and run a **production** release:

1. Add an environment variable `AMBER_ENV` with a value of `production`
2. Run these commands:

```
npm run release
amber db create migrate
shards build --production
./bin/crystal-api
```

## Docker Compose

To set up the database and launch the server:

```
docker-compose up -d
```

To view the logs:

```
docker-compose logs -f
```

> **Note:** The Docker images are compatible with Heroku.

## Contributing

1. Fork it ( https://github.com/aarek/crystal-api/fork )
2. Create your feature branch (git checkout -b my-new-feature)
3. Commit your changes (git commit -am 'Add some feature')
4. Push to the branch (git push origin my-new-feature)
5. Create a new Pull Request

## Contributors

- [aarek](https://github.com/aarek) Arkadiusz Oleksy - creator, maintainer
