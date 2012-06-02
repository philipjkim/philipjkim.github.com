---
layout: post
title: "cucumber-sinatra: Getting Started"
description: ""
category: 
tags: [Ruby]
---
{% include JB/setup %}
## Steps

1. Install [cucumber-sinatra](https://github.com/bernd/cucumber-sinatra) gem.

```$ gem install cucumber-sinatra```

2. Initialize the cucumber environment.

```$ cucumber-sinatra init --app MyApp lib/my_app.rb```
 * `MyApp` : the class name of your application
 * `lib/my_app.rb` : the path to the application file (required)

3. Check out the auto-generated app works properly.

 * Run `thin start`
 * Visit http://localhost:3000 and you should see "Hello MyApp!" on the page.

4. Write a plain text specifications to `features/my_app.feature`.

<pre>
Feature: view pages

  Scenario: Home page
    Given I go to the homepage
    Then I should see "Hello MyApp!"
</pre>

5. Run `cucumber features`, then you should see the following messages without errors.

<pre>
Feature: view pages

  Scenario: Home page                # features/my_app.feature:3
    Given I go to the homepage       # features/step_definitions/web_steps.rb:23
      Then I should see "Hello MyApp!" # features/step_definitions/web_steps.rb:107

1 scenario (1 passed)
2 steps (2 passed)
0m0.159s
</pre>

## References

- [https://github.com/bernd/cucumber-sinatra](https://github.com/bernd/cucumber-sinatra)

- [http://tooky.co.uk/2009/02/05/getting-started-with-cucumber-and-sinatra.html](http://tooky.co.uk/2009/02/05/getting-started-with-cucumber-and-sinatra.html)
