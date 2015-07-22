unholster-webapps cookbook
==========================

This is a central workspace that contain basics chef recipes and templates to be used in Unholster project's.

Recipes
-------

This repository have recipes to configure:

* PostgreSQL - [source](https://github.com/Unholster/chef-webapps/blob/master/recipes/database.rb)
* Redis servers - [source](https://github.com/Unholster/chef-webapps/blob/master/recipes/reddis.rb)
* FQDN services - [source](https://github.com/Unholster/chef-webapps/blob/master/recipes/fdqn.rb)
* User webapps - [source](https://github.com/Unholster/chef-webapps/blob/master/recipes/user.rb)
* Webapps - [source](https://github.com/Unholster/chef-webapps/blob/master/recipes/webapps.rb)


Templates
---------

Also can find default templates for lift this servers:

* Newrelic - [source](https://github.com/Unholster/chef-webapps/blob/master/templates/default/newrelic.erb)
* Nginx  - [source](https://github.com/Unholster/chef-webapps/blob/master/templates/default/nginx-site.erb)
* Redis - [source](https://github.com/Unholster/chef-webapps/blob/master/templates/default/redis.erb)

How to use
---------

1. This repo must be in the same path where you have your proyect (not inside this)
2. Create a Cheffile at the root of your project with this lines:
```ruby
site 'https://supermarket.getchef.com/api/v1'

cookbook 'unholster-webapps',
    :path => '../chef-webapps'
```
3. Set in your Vagtantfile (this must be at the root of your ptoject) this two lines:
```ruby
config.berkshelf.berksfile_path = "../chef-webapps/Berksfile"
config.berkshelf.enabled = true
```



```
{
    'foo': 'bar',
}
```
