# Fragment Caching:

## Code example:
```ruby
<% @products.each do |product| %>
  <% cache product, expires_in: 1.day do %>
    <%= render product %>
  <% end %>
<% end %>
```

- Should use *:expires_in* option.

## Logs:
```
Cache digest for app/views/products/_product.html.haml: 2378c5eeb5f3b622d13cc4365d18e282
```

## Russian Doll Caching

- That is nest cached fragments inside other cached fragments.
- Using *touch => true* to change updated_at for the associated things.  
  

## Check:
Rails.cache.data.keys ‘view*’

Or

Base on config config.cache_store in application.rb

```ruby
config.cache_store = :redis_store, { :host => ENV['REDIS_HOST'],
                                         :port => 6379,
                                         :db => 1}
```                                         

In rails console

```ruby
redis = Redis.new(host: ENV['REDIS_HOST'], port: 6379, db: 1) 
redis.keys
```


## Resources:

- http://guides.rubyonrails.org/caching_with_rails.html#fragment-caching

- https://github.com/rails/cache_digests
