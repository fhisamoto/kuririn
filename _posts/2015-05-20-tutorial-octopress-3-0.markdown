---
layout: post
title: "Tutorial Octopress 3.0"
date: 2015-05-20T21:42:31-03:00
---

# Instalação do Octopress 3.0 from scratch

Ou seja, estou assumindo que você não irá migrar de um Octopress 2.0.

## Install Octopress

Crie um Gemfile com as gems:

{% highlight ruby %}
source "https://rubygems.org"

gem 'octopress', '~> 3.0'
gem 'octopress-deploy'
{% endhighlight %}

eu prefiro deixar as gems e os binários no mesmo diretório, por isso

``$ bundle install --binstubs --path=vendor``

para criar um novo blog

``$ bundle exec octopress new <new_blog>``

### Novo blog octopress

A partir do diretório `new_blog`, então

``$ cd new_blog``

estará a estrutura do blog octopress 3.0 criada.

### Deployment no github

Criar um repositório no github com o nome __seu_usuario.github.io__. Então execute

``$ bundle exec octopress deploy init git <url>``,

exemplo:

``$ bundle exec octopress deploy init git git@github.com:usuario/usuario.github.io.git``

então, para fazer um deploy

``$ bundle exec octopress deploy``
