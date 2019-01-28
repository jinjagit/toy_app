# toy_app

Following the [Rails Tutorial](https://www.railstutorial.org/book/toy_app), by Michael Hartl, as part of the Odin Project's [Ruby on Rails unit](https://www.theodinproject.com/courses/ruby-on-rails/lessons/a-railsy-web-refresher).

[View live version.](https://vast-spire-64894.herokuapp.com/) (Can take up to 20 seconds to initialize). 

## issues encountered with tutorial (and workarounds):

  * Running <code>rails generate scaffold ... </code>, from section 2.2 of the tutorial, gave an error complaining of lack of 'bootsnap' gem. resolved by adding <code>gem 'bootsnap',     '1.1.2'</code> to Gemfile, and running <code>bundle install --without production</code> and <code>bundle update</code>.
  * Running <code>rails generate scaffold ... </code>, from section 2.2 of the tutorial, gave an error complaining of wrong rails version. Resolved by editing Gemfile rails version to: <code>gem 'rails',        '~> 5.2.0'</code> (to match my installed version), and running <code>bundle install --without production</code> and <code>bundle update</code>.
  * Running <code>rails db:migrate</code> gave multiple warnings related to fileutils gem: 'warning: already initialized constant FileUtils::<constant>'. Resolved by following solution [here](https://stackoverflow.com/questions/51334732/rails-5-2-0-with-ruby-2-5-1-console-warning-already-initialized-constant) (uninstall / reinstall gem). At this point, running <code>rails server</code> and visiting app locally in browser showed 'hello, world!' message, (with no warnings / errors), as expected by tutorial.
