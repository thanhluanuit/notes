# Twilio API

Products:
- SMS
- Voice
- Video

Gem: https://github.com/twilio/twilio-ruby

Price: https://www.twilio.com/sms/pricing

Document:
- https://www.twilio.com/docs/ 
- https://www.twilio.com/docs/libraries/ruby

Demo:

```ruby
require 'twilio-ruby'


account_sid = "AC320edac14390dcc4a9f6f9842424c2a3" # Your Account SID from www.twilio.com/console
auth_token = "your_auth_token"   # Your Auth Token from www.twilio.com/console


@client = Twilio::REST::Client.new account_sid, auth_token
message = @client.messages.create(
    body: "Hello from Ruby",
    to: "+12345678901",    # Replace with your phone number
    from: "+12345678901")  # Replace with your Twilio number

puts message.sid
```
