# Google Analytics API

1. Go to: https://console.developers.google.com
	
2. Click 'Create Project'

3. Enable 'Analytics API'
![Enable Analytics API](/images/ga-1.png)

4. Create an ‘OAuth 2.0 client IDs’ (Application type is Other)
![Create Credentials](/images/ga-2.png)

5. Go to  Google Analytics account: http://www.google.com/analytics/

6. Add user email to GA permission.
![Add permission to email](/images/ga-3.png)

7. Go to Query Explore to test: https://ga-dev-tools.appspot.com/query-explorer/	

> Notes: Get PROFILE_ID from ids: ga:xxxxxxxxx


8. Documents:
https://developers.google.com/api-client-library/


# Integrate with Ruby

- Gem: [google-api-ruby-client](https://github.com/google/google-api-ruby-client)

- Samples: [analytics.rb](https://github.com/google/google-api-ruby-client/blob/master/samples/cli/lib/samples/analytics.rb)

