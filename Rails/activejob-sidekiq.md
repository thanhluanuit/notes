# Active Job with Sidekiq

## Active Job
- Active Job is a framework for declaring jobs and making them run on a variety of queuing backends. 

- Rails by default comes with an asynchronous queuing implementation that runs jobs with an in-process thread pool. Jobs will run asynchronously, but any jobs in the queue will be dropped upon restart.

- Active Job has built-in adapters for queuing backend as:
    - Sidekiq
    - Resque
    - Delayed Job
    - Others


## Sidekiq

- Sidekiq is a full-featured background processing framework for Ruby.

- Sidekiq uses threads to handle many jobs at the same time in the same process. 


## Usage

1. Add gem 'sidekiq'

2. Add sidekiq.rb to config/initializers/

```ruby
Sidekiq.configure_server do |config|
  config.redis = { url: 'redis://localhost:6379' }
end

Sidekiq.configure_client do |config|
  config.redis = { url: 'redis://localhost:6379' }
end
```

```
Redis url format: 'redis://[ip-host]:[port]'
```

3. Setting queue adapter in config/application.rb

```ruby
module SidekiqApp
  class Application < Rails::Application
    # Be sure to have the adapter's gem in your Gemfile
    # and follow the adapter's specific installation
    # and deployment instructions.
    config.active_job.queue_adapter = :sidekiq
  end
end
```

4. Advance configuration: config/sidekiq.yml
```
:verbose: true
development:
  :concurrency: 1
production:
  :concurrency: 20
:queues:
  - critical
  - default
  - mailers
  - low
:timeout: 60
```


## Resources:

- http://guides.rubyonrails.org/active_job_basics.html

- https://github.com/mperham/sidekiq/wiki/Active-Job

## Demo
- https://github.com/thanhluanuit/sidekiq-activejob
