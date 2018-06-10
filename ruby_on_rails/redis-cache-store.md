# Redis Cache Store 

- Redis Cache Store is a new feature on Rails 5.2.
- The Redis cache store takes advantage of Redis support for automatic eviction when it reaches max memory, allowing it to behave much like a Memcached cache server.

Add redis gem to Gemfile

```ruby
  gem 'redis'
```

You can enable support for the faster hiredis connection library by additionally adding its ruby wrapper to your Gemfile:

```ruby
  gem 'hiredis'
```

Finally, add the configuration in the relevant config/environments/*.rb file:

```ruby
  config.cache_store = :redis_cache_store, { url: ENV['REDIS_URL'] }
```

Check redis keys on Rails console:

```ruby
  Rails.cache.redis.keys
```

## Caching in Development:

- It's common to want to test the caching strategy of your application in development mode. 
- Rails provides the rake task dev:cache to easily toggle caching on/off.

```ruby
$ bin/rails dev:cache
Development mode is now being cached.

$ bin/rails dev:cache
Development mode is no longer being cached.
```


## Resources:
- Doc: http://guides.rubyonrails.org/caching_with_rails.html#activesupport-cache-rediscachestore
- Demo: https://github.com/thanhluanuit/redis-cache-store

