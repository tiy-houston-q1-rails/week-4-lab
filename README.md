Week 4 Lab - Rails Dynamic Pages
-------------------------------

Goals:
----

* Able to create a rails app
* Style the rails app using the asset pipeline
* Use the Router (config/routes) to have a dynamic set of pages
* Pass data from the controller to the views to render


Requirements:
----

1. Craft a Rails app that shows your Surf and Paddle (can expand from day 18)
1. Make the pages dynamic, where:
  * The root page shows the latest post
  * The images at the bottom of the page link link to that post
  * When viewing that post (URL will be /posts/:permalink) it shows that post


posts should be something like this:

```ruby
Post = Struct.new(:permalink, :image_name, :content)
@posts = []
@posts << Post.new("waffles-are-best", "waffles.jpg", "waffles are the best...")
@posts << Post.new("pancakes-are-best", "pancakes.jpg", "pancakes are the best...")
@posts << Post.new("bacons-are-best", "waffles.jpg", "waffles are the best...")
```

Notes:
-----

* `Struct` is an easy way to define a class. You can just use a hash, or a real
  class if you want
* To find an element in your `@posts` array, use `@posts.find {|p| p.permalink
  == params[:permalink]}` or similar
* There is no database in this lab, but we will have databases next week.
