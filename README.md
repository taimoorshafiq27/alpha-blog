<!-- # README

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

* ... -->

SETUP
create web app with $ rails new <app_name>
git is initialised when app is created
$ git add -A
$ git commit -m "Initial commit and add root route"
create github repo and link with git using $ git remote add origin <url>

ROOT ROUTE
create pages dir in View dir
create home.html.erb file which will be the homepage i.e. root page
create pages_controller.rb file in Controllers dir
add home action to pagescontroller file
edit root route in /config/routes.rb
root <'controller#action'>

ABOUT PAGE
create about.html.erb file in pages dir
add about action to pagescontroller file
create about page in Pages dir
add route to routes.rb

--OPTIONAL--
create heroku account to deploy app
install heroku CLI tools
log in with heroku CLI
to create heroku app $ heroku create
edit gemfile to cut sqlite3 and paste it into development, test block (sqlite3 good for development, not for production)
then add production block. heroku works with pg (ruby interface to the PostgreSQL db that heroku works with)

group :production do
  gem 'pg'
end

$ bundle install --without production

$ git add -A
$ git commit -m "Make app production ready"
$ git push heroku main

rename heroku app in CLI