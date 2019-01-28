# toy_app

Following the [Rails Tutorial](https://www.railstutorial.org/book/toy_app), by Michael Hartl, as part of the Odin Project's [Ruby on Rails unit](https://www.theodinproject.com/courses/ruby-on-rails/lessons/a-railsy-web-refresher).

## issues encountered with tutorial (and workarounds):

  * Running <code>rails generate scaffold ... </code>, from section 2.2 of the tutorial, gave an error complaining of lack of 'bootsnap' gem. resolved by adding <code>gem 'bootsnap',     '1.1.2'</code> to Gemfile, and running <code>bundle install --without production</code> and <code>bundle update</code>.
  * Running <code>rails generate scaffold ... </code>, from section 2.2 of the tutorial, gave an error complaining of wrong rails version. Resolved by editing Gemfile rails version to: <code>gem 'rails',        '~> 5.2.0'</code> (to match my installed version), and running <code>bundle install --without production</code> and <code>bundle update</code>.
  * Running <code>rails db:migrate</code> gave multiple warnings related to fileutils gem: 'warning: already initialized constant FileUtils::<constant>'. Resolved by following solution [here](https://stackoverflow.com/questions/51334732/rails-5-2-0-with-ruby-2-5-1-console-warning-already-initialized-constant) (uninstall / reinstall gem). At this point, running <code>rails server</code> and visiting app locally in browser showed 'hello, world!' message, (with no warnings / errors), as expected by tutorial.

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
