# Data Normalization

## Objectives

1. Understand why we as programmers need to manipulate and format data.
2. Learn how to format file names. 
3. Learn about writing data to files using Ruby. 

## Data Normalization

As programmers, it's our job to deliver information to people. We are being entrusted with an enormous responsibility––to handle people's data (whether it's videos, music, insurance information, pictures of cats, etc.) and deliver it to them in a clean, sensical manner. One very common action that you'll likely facilitate as a programmer is that of downloading files, such as audio files. Normal people like their files titled in normal ways. `artistSongxy1288304` doesn't mean anything to the muggles (non-progammers) of the world. In this lab, we'll be taking file names, normalizing them and writing their contents to a file in a `tmp` folder. 

## Writing Data to Files in Ruby

Ruby makes it easy to write data to a file. Ruby has a built-in [File class](http://ruby-doc.org/core-2.2.2/File.html). You can create new temporary files using: 

`Tempfile.new`

The `.new` method can take in a number of arguments. The first argument is an array. The first element of that array is the file name and the second argument of the array is the file extension/type. The second argument is the desired location of the file. Let's take a look: 

```ruby
my_file = Tempfile.new(["my_new_file", ".txt"], "desktop/my_awesome_folder")
```

You can then write to that file using the `.write` method. The `.write` method takes in an argument of the content you want to write the the file. Let's take a look:

```ruby
my_file.write("some awesome content for my awesome new file")
```

Use the documentation linked to above, along with the tips outlined here, to solve the lab that follows this reading. 

## Resource Naming Conventions and Slugification 

As programmers, we don't write code for computers, we write code for humans. Our job is to make the programs we write as easy and even pleasurable to use as possible. One of the key areas in which we enact this principle is naming––naming files, naming URLS, you name it! Consequently, there are certain conventions we want to follow when naming our files. A file that contains a song is likely going to be called `song_title.mp3`. A file that contains a picture is likey to be called something like `profile_pic.png`. These file names are often referred to as **"slugs"**. A slug can refer to a resource name or location that is "human readable". We'll encounter the concept of slugs later on when we learn about the web.

<a href='https://learn.co/lessons/data-normalization-reading' data-visibility='hidden'>View this lesson on Learn.co</a>
