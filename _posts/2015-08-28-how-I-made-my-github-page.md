---
layout: post
title: How I made a static blog site with GitHub Pages and Jekyll.
---

<div class="message">
  Welcome to my blog. Check out how I made a static site with GitHub.
</div>

On this post I'm going to walk through how I set up my site. 

### Installation Requirements:

- [GitHub Account](https://github.com/join)

- [GitHub Page](https://help.github.com/articles/creating-pages-with-the-automatic-generator/)

- [Ruby](https://www.ruby-lang.org/en/downloads/)

- [Bundler](http://bundler.io/)

- [Jekyll](http://jekyllrb.com/)

- [NodeJS](https://nodejs.org/)


### Additional Tools:

- [Git Bash](https://git-scm.com/downloads)

Gladly, the documentation for building with [GitHub Pages](https://pages.github.com/) and how to [Run Jekyll on Windows](http://jekyll-windows.juthilo.com/) are available and a great resource to learn from. Read carefully about the installion requirements for each program you need to install for the system you are working on. Now to get started.


### Step 1. Clone Repository

Once your account is created you will need to make a [new repository.](https://github.com/new) Clone the repository to your local directory. Create an html file and push the commit. Now you have a working repository and can move on to getting ruby set up.

### Step 2. Install Ruby

Ruby has specific system requirements. Once you have ruby setup and running it will help build the gem dependencies you will need for Jekyll. Since I'm working with Windows 8.1 I went with [RubyInstaller](https://www.ruby-lang.org/en/documentation/installation/#rubyinstaller) Ruby 2.0.0-p645 (x64) and [DevKit](http://rubyinstaller.org/downloads/) that corresponds with my installed version of Ruby. 

Dowload RubyInstaller and check “Add Ruby executables to your PATH” box. If you'd like to read more about working with [Ruby on Windows](http://rubyonwindowsguides.github.io/book/ch02-01.html) this is a great guide which explains indepth the install process. 

Once you have installed the DevKit navigate to it's config.yml file and edit for the version of Ruby you are using. 

{% highlight js %}
//# Example of my config.yml file:
- C:/Ruby200-x64
{% endhighlight %}

Now open up a command line editor and initialize the DevKit in the folder you extracted it to. Type:

{% highlight js %}
ruby dk.rb init
{% endhighlight %}
Then,
{% highlight js %}
ruby dk.rb install
{% endhighlight %}


Should you receive an error, read it carefully. If you have missed something the error message may assist you in resolving the problem. 

### Step 3. Install Bundler and Jekyll

Bundler and Jekyll are gems that allows you to build with Ruby. You can install gems through any command line or bash console. For installation type:

{% highlight js %}
$ gem install jekyll
{% endhighlight %}

<blockquote>
<p>Compatibility Note: Do not attempt to install Jekyll v1.4.3, though, which is known to be <a href="https://github.com/jekyll/jekyll/issues/1948">incompatible with Windows.</a></p>
</blockquote>


{% highlight js %}
$ gem install bundler
{% endhighlight %}

Add to Gemfile configuration:

{% highlight js %}
source 'https://rubygems.org'
gem 'github-pages'
{% endhighlight %}

Now to install your site build:

{% highlight js %}
$ jekyll new my-site
$ cd my-site
/my-site $ bundle exec jekyll serve
=> Now browse to http://localhost:4000
{% endhighlight %}

At this point you should have a fully functional site build. Add themes and edit it to your hearts content. 