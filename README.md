# Zendesk API Client
## Configuration

Configuration is done through a block returning an instance of {Zendesk::Client}.
The block is mandatory and if not passed, a {Zendesk::ConfigurationException} will be thrown.

```
Zendesk.configure do |config|
  # Mandatory:

  # Must be https URL unless it is localhost or 127.0.0.1
  config.url = "https://mydesk.zendesk.com"

  # Optional, but recommended:

  config.username = "test.user"
  config.password = "test.password"

  # Truly optional:

  # Retry uses middleware to notify the user
  # when hitting the rate limit, sleep automatically,
  # then retry the request.
  config.retry = true
  # Log prints out requests to STDOUT
  config.log = true
end
```

Note: This Zendesk API client only supports basic authentication at the moment.

## Usage

The result of configuration is an instance of {Zendesk::Client} which can then be used in two different methods.

## Note on Patches/Pull Requests
1. Fork the project.
2. Make your feature addition or bug fix.
3. Add tests for it. This is important so I don't break it in a future version
   unintentionally.
4. Commit, do not mess with rakefile, version, or history. (if you want to have
   your own version, that is fine but bump version in a commit by itself I can
   ignore when I pull)
5. Send me a pull request. Bonus points for topic branches.

## Supported Ruby Versions

## Copyright