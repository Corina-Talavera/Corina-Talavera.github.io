---
layout: post
title:      "Simplifying classes in Ruby"
date:       2019-01-03 16:13:18 +0000
permalink:  simplifying_classes_in_ruby
---



Classes serve as blueprint for objects. When creating a class, it is key to keep in mind what is the class doing and what does the class know. What the class knows are instant variables and what the class does are methods. 

Example: 
class Cat  
  def initialize(breed, name)  
    @breed = breed  
    @name = name  
  end  
  
  def meow  
    puts "Meow. I'm a cat."  
  end  
end  


In this case what the Cat class knows is the breed and name. What the class does is Meow.
  
