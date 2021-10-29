# App

## Setup

### prerequirement

* ruby (see .ruby-version)
* postgresql dev library
  * macOS: `brew install libpq`
  * archlinux: `yay -S postgresql-client`
* docker
* docker-compose
* direnv ( https://github.com/direnv/direnv )
* yarn

### Setup

direnv

```
cp .envrc.sample .envrc
direnv allow
```

bundle

```
bundle config set path 'vendor/bundle'
bundle binstubs --path=vendor/bundle/bin

`bundle binstubs` needs at least one gem to run. #この出力は無視

bundle install -j4
```

create DB

```
docker-compose up -d

rails db:create
rails db:migrate
```

yarn install

```
yarn install
```

### Run server

```
bin/server
```

### Run rspec

```
rails spec
```

### Run rspec with guard

```
guard
```

