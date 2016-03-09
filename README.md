#MongoDB Setup

##Installing
install mongoDB:
```bash
brew install mongodb
```

setup db:
```bash
sudo mkdir -p /data/db
```

change ownership:
```bash
sudo chown -R `id -u` /data/db
```

##Starting Service

start mongoDB service:
```bash
mongodb
```

start mongo shell:
```bash
mongo
```

##Sample data

Grab zips set:
```bash
curl http://media.mongodb.org/zips.json > ./zips.json
```

Import the json to database:
```bash
mongoimport --db test --collection zips --drop --file zips.json
```

##Ruby Gems to integrate MongoDB
```ruby
gem update
gem install mongo
gem install bson_ext
```

##Elixir hex to integrate MongoDB
mix.exs:
```elixir
{:mongo, "~> 0.5.4"},
{:mongodb, "~> 0.1.1"}
```
