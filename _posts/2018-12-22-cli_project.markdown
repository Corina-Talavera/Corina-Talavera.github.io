---
layout: post
title:      "CLI Project"
date:       2018-12-22 16:32:40 +0000
permalink:  cli_project
---


When I was growing up, one of my favorite movies to watch on repeat was Studio Ghibli’s Spirited Away. I had almost every line memorized. I thought it would be a lot of fun with this project to do an homage to Studio Ghibli!

How I decided to approach this was to scrape an API and from there see a list of films, descriptions, and the Rotten Tomatoes scores. 


Step 1: Install Bundler Gem

Seriously. This saved me so much time and energy in creating individual folders.

To create a gem using Bundler you type “bundle gem insertnameofproject”

Step 2: Adding executable files

This is within the bin file that way I have a place to run my program. 

Add the shebang ( aka how the file knows what language to run!) 
#!/usr/bin/env ruby
Require relative ‘../lib/studio_ghibli’
CLI.new.call

Make the file executable by using chmod. Thi is a command and system call which can access permissions to the file systems! This is important to have others use your program
$ chmod +x <file_name>

Step 3. Preparing the files!

I am  the type that likes to build a skeleton within the lib first. I knew I was going to need a CLI file, the scraper/API file, and a file for the films. 

Within studio_ghibli.rb I needed to set up the environment. 
Ex: 
require 'pry'
require 'nokogiri'
require 'open-uri'
require 'json'

require_relative 'studio_ghibli/api'
require_relative 'studio_ghibli/film'
require_relative 'studio_ghibli/cli'
require_relative 'studio_ghibli/version'

Step 4: Gemspec

The gemspec should also be updated to include a small summary, description, and homepage/github page. Be sure to add dependencies like “Nokogiri”

Step 5: Scrape the data!
In my case, I am using the Studio Ghibli API. So, why an API vs scraping a website? The information appears much cleaner in my opinion and serves as a better building block for parsing out the data. If you're interested in more information on APIs, this wiki page was helpful for me! [https://en.wikipedia.org/wiki/Application_programming_interface]

 Step 6: Creating the CLI 

I know in order to create the CLI interface, I am going to need to need to define a class  like "CLI”. What I want this CLI to have a welcome message, list the films, circle back to the menu, and an exit. From there I will need to define each of these features. 


My goals with this project is to keep the interface simple and to help share my love of Studio Ghibli films!

