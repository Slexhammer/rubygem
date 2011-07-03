# The Official Poll Everywhere API Gem

The Poll Everywhere gem is the best way to integrate Poll Everywhere with your applications.

## Getting Started

Install the Poll Everywhere rubygem:

    $ sudo gem install polleverywhere

If you're using bundler, add the following line to your Gemfile:

    gem "polleverywhere"

## Accessing your polls

    require 'polleverywhere'
    
    # Specify your username and password here
    PollEverywhere.config do
      username  "my_username"
      password  "my_password"
    end
    
    # Create a multiple choice poll
    ftp = PollEverywhere::MultipleChoicePoll.new
    ftp.title = 'Do you love numbers?'
    ftp.options = %w[1 2 3]
    ftp.save
    
    # Create a free text poll    
    mcp = PollEverywhere::FreeTextPoll.new
    mcp.title = 'What is your favorite thing about vacation?'
    mcp.save
    
    # Now start playing! Get a list of your polls
    polls = PollEverywhere::Poll.all
    
    # ... or grab a specific poll
    mcp2 = PollEverywhere::MultipleChoicePoll.get(':permalink')

You can do all sorts of fun stuff with polls!

## Additional resources

* **API Documentation** - http://api.polleverywhere.com
* **RDocs** - http://rubydoc.info/gems/polleverywhere
* **Mailing list** - http://groups.google.com/group/polleverywhere-dev
* **Professional Support** - http://www.polleverywhere.com/professional-support
* **API & RubyGem Roadmap** - https://github.com/polleverywhere/polleverywhere/issues/milestones

## Goals & Roadmap

In the future, you can expect:

* API models and documentation for areas of Poll Everywhere
* Process errors triggered by the server
* Perform client-side validations
* Asyn/Evented HTTP adapter
* App-layer specs
* Protocol/API-layer specs

## Professional Development & Support

If you'd like for us to implement part of Poll Everywhere as a documented API or RubyGem and you don't see it on here, please engage our professional support services at http://www.polleverywhere.com/onsite-and-dedicated-support#custom_solutions.