
```terminal:terminal
docker-compose run app rails new . --force --database=mysql
```


```rails:database.yml
default: &default
  adapter: mysql2
  encoding: utf8mb4
  pool: <%= ENV.fetch("RAILS_MAX_THREADS") { 5 } %>
  username: <%= ENV['MYSQL_USER'] %>
  password: <%= ENV['MYSQL_PASSWORD'] %>
  host: localhost
```


```rails:Gemfile
gem 'dotenv-rails'
```

```terminal:terminal
docker-compose build
```

```terminal:terminal
docker-compose up -d
```


