---
layout: post
title: How I made a static blog site with GitHub Pages and Jekyll
---

<div class="message">
  Welcome! Check out how I made a static site with GitHub.
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

Gladly, the documentation for building with [GitHub Pages](https://pages.github.com/) and how to [Run Jekyll on Windows](http://jekyll-windows.juthilo.com/) are available and a great resource to learn from. Read carefully for installion requirements on the software your system needs. Now to get started.

<blockquote>
<p>Site Build Note: A <a href="https://en.wikipedia.org/wiki/Static_web_page">static web page</a></p> is a stationary site that does not render dynamic content through a web application.
</blockquote>


### Step 1. Clone Repository

Once your account is created you will need to make a [new repository.](https://github.com/new) Clone the repository to your local directory. Create an html file, add and push the commit. Now you have a working repository and can move on to getting ruby set up.

### Step 2. Install Ruby

Ruby has specific system requirements. Once ruby is setup and running it will help build the gem dependencies you will need for the Jekyll gem. Since I'm working with Windows 8.1 I went with [RubyInstaller](https://www.ruby-lang.org/en/documentation/installation/#rubyinstaller) Ruby 2.0.0-p645 (x64) and [DevKit](http://rubyinstaller.org/downloads/) that corresponds with the installed version of Ruby. 

Dowload RubyInstaller and check “Add Ruby executables to your PATH” box. If you'd like to read more about working with [Ruby on Windows](http://rubyonwindowsguides.github.io/book/ch02-01.html) this is a great guide which explains indepth the install process. 

Once you have installed the DevKit navigate to it's config.yml file and edit for the version of Ruby you are using. 

```
# Example of my config.yml file:

---
- C:/Ruby200-x64

```

Now open up a command line editor and initialize the DevKit in the folder you extracted it to. Type:

```
ruby dk.rb init

```

Then,

```
ruby dk.rb install
```


Should you receive an error, read it carefully. If a step was missed during the installion process an error message may assist you in debugging the problem. 

### Step 3. Install Gems

Bundler and Jekyll are gems that allows you to build with Ruby. You can install gems through any command line or bash console. For installation type:

```
$ gem install jekyll
```

<blockquote>
<p>Compatibility Note: Do not attempt to install Jekyll v1.4.3, though, which is known to be <a href="https://github.com/jekyll/jekyll/issues/1948">incompatible with Windows.</a></p>
</blockquote>


```
$ gem install bundler
```

Add to Gemfile configuration:

```
source 'https://rubygems.org'
gem 'github-pages'
```

Install site build:

```
$ jekyll new my-site
$ cd my-site
/my-site $ bundle exec jekyll serve
=> Now browse to http://localhost:4000
```

At this point there should be a fully functional site build. Begin adding specifics by editing the _config.yml file. Jekyl comes with additional [plugins](http://jekyllrb.com/docs/plugins/) and [themes.](http://jekyllthemes.org/) 