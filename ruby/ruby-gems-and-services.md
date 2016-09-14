# A LIST OF RUBY GEMS AND SERVICES 

## Helpers

1. Form helper
 * [simple_form](https://github.com/plataformatec/simple_form)  
2. Pagination
 * [Kaminari](https://github.com/amatsuda/kaminari)  
3. Adding Markdown to longer text  
 * [RDiscount](https://github.com/davidfstr/rdiscount)  
4. Pretty URLs  
 * [Stringex](https://github.com/rsl/stringex)  
5. Tagging  
 * [act-as-taggable-on](https://github.com/mbleigh/acts-as-taggable-on)  
6. Date parsing  
 * [Chronic](https://github.com/mojombo/chronic)  
7. Undo things after editing (e.g., deleting)  
 * [Paranoia](https://github.com/rubysherpas/paranoia)
8. Mute assets pipeline log messages.
 * [quiet_assets](https://github.com/evrone/quiet_assets)

## Geolocation
1. [Geocoder](http://www.rubygeocoder.com/)  
2. [leaflet.js](http://leafletjs.com/)
3. [Mapbox](https://www.mapbox.com/)  

## Administration  
1. Content management  
 * [Active Admin](http://activeadmin.info/)  
2. Customer management (e.g. queries, newsletters, auto-emails, etc.)  
 * [Intercom](https://www.intercom.io/)  

## Uploads
1. Image and file uploads  
 * [Paperclip](https://github.com/thoughtbot/paperclip)  
2. Add file uploads to [Amazon S3](http://aws.amazon.com/)  
 * [aws-sdk](http://aws.amazon.com/sdk-for-ruby/)  

[A guide to Heroku, Paperclip and S3](https://devcenter.heroku.com/articles/paperclip-s3)  

## Search  
1. Adding search to a site  
 * [Algolia](http://www.algolia.com/)  
2. [Simple ElasticSearch client for ruby](https://github.com/printercu/elastics-rb)  
3. [Ruby integrations for Elasticsearch](https://github.com/elastic/elasticsearch-ruby)  
4. [Rails simple search](https://github.com/yzhanginwa/rails-simple-search)

[Algolia demos](https://www.algolia.com/demo/autocomplete)  

## User systems
1. Authentication  
 * [Device](https://github.com/plataformatec/devise)
 * [Omniauth](https://github.com/intridea/omniauth) **(e.g. any kind of social login)**
2. Properly case people's names  
 * [Namecase](https://github.com/tenderlove/namecase)  
3. Authorization (add in user roles)
 * [Cancan](https://github.com/ryanb/cancan)  

## Accepting payments  
1. [Stripe](https://stripe.com/)

[Javascript documentation](https://stripe.com/docs/custom-form)  
[Ruby introduction](https://stripe.com/docs/api/ruby#intro)  

2. [GoCardless](https://gocardless.com/)  

[GoCardless documentation](https://github.com/gocardless/gocardless-ruby)  

## User Testing
1. [A/B Testing](https://en.wikipedia.org/wiki/A/B_testing)  
 * [Split](https://github.com/splitrb/split)  

Relies on [Redis](http://redis.io/) - use the [openredis](https://openredis.com/) Heroku add-on to use it.  

## APIs
1. To do any kind of scrapping use [HTTParty](https://github.com/jnunemaker/httparty) and [Nokogiri](http://www.nokogiri.org/) together.  
Use HTTParty to grab the content from the 3rd party site, then use Nokogiri to turn it into something I can parse.  

2. Gems for social networks  
 * [Twitter gem](https://github.com/sferik/twitter)
 * [Koala for Facebook](https://github.com/arsduo/koala)  

3. For any kind of real time systems (e.g. a chat site or an online game), look into [Pusher](https://pusher.com/)  

## Notifications
1. For voice and messaging applications with [Twilio](https://www.twilio.com/) use [twilio-ruby](https://github.com/stevegraham/twilio-rb)  

2. For notification in chat rooms
 * [slack-notify](https://github.com/sosedoff/slack-notify) for [Slack](https://slack.com/)
 * [hipchat-rb](https://github.com/hipchat/hipchat-rb) for [HipChat](https://www.hipchat.com/)

## Emails
1. For sending out emails use [Sendgrid](http://sendgrid.com/)
2. Making HTML emails use [Roadie](https://github.com/Mange/roadie)

## Errors
1. For real time crash reporting use [Sentry](https://getsentry.com/welcome/)
2. For log management use [Papertrail](https://papertrailapp.com/)
3. For development debugging use [better_errors](https://github.com/charliesome/better_errors) you may install it with [binding_of_caller](https://github.com/banister/binding_of_caller)

## Testing  
1. Automated testing
 * [Minitest](https://github.com/seattlerb/minitest)
 * [RSpec](https://github.com/rspec/rspec)

2. Integration tests
 * [Capybara](https://github.com/jnicklas/capybara)

3. For making test data use [Factory Girl](https://github.com/thoughtbot/factory_girl_rails)

4. File system modifications (e.g. testing something that you just leave running in the background) use [Guard](https://github.com/guard/guard)  

5. [VCR](https://github.com/vcr/vcr) (a way to test with APIs)

6. [Timecop](https://github.com/travisjeffery/timecop) (a way to freeze and fast forward time)

7. [Code Climate](https://codeclimate.com/) Monitor the health of your code from command line to the cloud 

## Deployment
If you use [Heroku](https://www.heroku.com/) for deployment, you may have to set up three different servers to have different environments to test with. They are development (trying out things), production (the live site) and staging (same database as production but to try out code before it goes live). To do this use [heroku_san](https://github.com/fastestforward/heroku_san) gem. All you need to do to deploy to staging is:  

```ruby
rake staging deploy
```  

To make sure your code is super quick use [New Relic](http://newrelic.com/) to monitor speeds and spot any slow areas of sites.  
Use caching on production using the [dalli](https://github.com/petergoldstein/dalli) gem with [Memcachier](https://www.memcachier.com/).  
Running scheduled tasks use [Heroku Scheduler](https://elements.heroku.com/addons/scheduler) add-on.
