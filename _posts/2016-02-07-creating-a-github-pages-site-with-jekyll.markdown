---

layout: post
title:  "Creating a Github Pages Site with Jekyll"
date:   2016-02-06 22:20:39 -0500
categories: jekyll

---

This is the start of my tech blog so I thought why not describe the steps it took to create it? The tasks were trivial maybe but not obvious.

Here goes:

* install Ruby
* install Bundler
* install Jekyll


Go to the directory where you want to put your site directory
{% highlight bash %}
$ jekyll new your-site-name
$ cd your-site-name
$ git init
$ git commit -m "initial"
{% endhighlight %}

Create a Gemfile

Add

{% highlight ruby %}
source 'https://rubygems.org'
gem 'github-pages'
{% endhighlight %}

Run
{% highlight bash %}
$bundle install
{% endhighlight %}

To see that the install went correctly run

{% highlight bash %}
$bundle exec jekyll serve
{% endhighlight %}

Go to your browser and navigate to http://127.0.0.1:4000/.

You will see a generic Jekyll page. you can start personalizing the site by editing the _config.yml. [The official instructions are pretty good][github-config]


To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[github-config]: https://help.github.com/articles/using-jekyll-with-pages/#configuring-jekyll


