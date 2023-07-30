---
layout: post
title: 'Weekly 0: Introduction'
date: 2023-07-30 11:13 +0800

img_path: /assets/Weekly/Weekly0
toc: true

image:
  path: conway.gif
  alt: Preview Image

---


## What are Weeklies?

Hi! Welcome to the the first post in a new series I started titled 'Weeklies'. Weeklies are short update posts published every Sunday, hence the name.

The nature of these Weeklies posts is simple: they will be used to describe progress in my projects that do not warrant their own posts. Examples of such topics may include learning about a new computer science concept or interesting historical trivia, optimizing or refactoring some functions in a bigger codebase, or coding small toy projects as a way to learn a less familiar language, such as how I recently created Conway's Game of Life in Python.

These posts will also be written in a more loose and less edited style too, allowing them to be finished at a comfortable pace with the tighter deadline. This format also allows me to keep the site active and alive in between bigger article posts, where I would want to spend more time drafting, editing and planning.

## Reflection

It's been two months since I started making taking this personal site seriously and in chose two months I had written a lot, scrapped a lot and ultimately learned a lot. I even changed Jekyll layouts, and still have a ton of articles to move over and improve.

![Blog Draft](blog_drafts.png)

When I first started, I imposed a weekly deadline for blog posts. At the time I wasn't quite sure of the quality and content of what I wanted to write, so once a week was a good way to experiment with different styles and work discipline. I found that meeting the deadline wasn't an issue for me but having only a week to draft and edit posts created a feeling of being too rushed, and some posts suffered in quality from it.

I noticed that I was particularly happy with the following posts compared to the others due to their more organized structure, topic matter and overall polish.
- My experiences using Fwog
- Using external programs to create levels instead of making in-engine editors

As such, I want to strive towards reaching that level of quality as a minimum for future articles, and so decided that they should have a longer deadline of about a month so that they can go through more iterations and research. 

Of course, I also noticed that there were perks to having a shorter deadline, the main one being that it allowed me to 'get stuff done', that is forced me to reflect more with new ideas to write about, and it encouraged me to not be too much of a perfectionist by meeting a deadline. 

Through this realisation, I figured that a 'best of both worlds' approach is to simply create a category of posts specifically for a weekly update (like this one) while allowing more time for full articles.

## What have I been up to coding wise?

### Less distractions

I made a new habit for myself to improve my productivity, focus and discipline by reducing my social media usage. 

The rules are simple. I can't access Discord public servers on any day that isn't Sunday and I also have Reddit and Twitter (I guess that is called X now?) blocked other than on Sunday. I also use the Unhook extension with Youtube in order to hide recommended and comments, which are also a source of distraction.

I found that with these simple lifestyle changes, I was spending my time more productively and less distracted. I was coding, studying and exercising more. I do recommend trying it, although I do have tendencies to get carried away with writing a lot. I now use my journal as an outlet for documenting my thoughts, rather than social media.

Here is an example of what my Youtube would look like now if say I want to listen to some music.

![Unhook Example](unhook.png)


### Solo Sprint with Plane Game

I have been working on continuing the Plane Game using Unity instead of my own engine. This is because the goals for Plane Game has changed to be more focused on making a fun and playable game that can be easily distributed rather than an outlet to practice programming skills. 

I will write more about it in future posts, but for short I have a 'Sprint' style workflow for it where I do a Daily standup Scrum meeting for my progress on it. I need to try out the system for a bit longer before I write a review but I was able to meet all the milestones I allocated for the first two week sprint I had set for myself so far, which shows promises.

![Plane Game Unity](plane_game.png)

## Python and Pygame

Lately I have been working on languages and frameworks I am not as familiar with compared to C++, which I use daily since starting undergrad. In particular, I have been playing around with Python using the Pygame library, which is a wrapper around SDL for Python. I also have been doing a bit of JavaScript in different forms, but not as much yet. 

For the Pygame projects, I worked on two things in order to get my feet wet with the language and the framework, a clone of Breakout and a Conway's Game of Life script. I chose to do them without using any tutorials or guides to hold my hand, only relying on documentation of the Pygame library and official Python documentation and manual. 

One thing to note is that Pygame is, despite its name, not a game framework like Phaser or Monogame. All I was given 'for free' is stuff like mouse and keyboard events, audio, simple AABB collision detection with rectangles that can also be rendered, loading in sprites and fonts for rendering, and the ability to blit to the framebuffer if I had hardware acceleration. It does not have a physics engine or scene management.

### Breakout

![Preview of Breakout](breakout.png)

Breakout refers to the 'single player' Pong clone that is common, where the paddle must hit the ball against blocks rather than another player. I prefer this compared to regular Pong as it is single player and the breakable blocks provide a bit more interesting features such as the potential of serialized levels.

For Breakout, it was simple for me and I completed it spread out a few days with around four hours of total working time. One of the challenges that was fun to work on was figuring out how to simplify and approximate the normal force reaction of a 'bounce' by myself. I ended up implementing this strange system where I checked for whether the horizontal or vertical adjacent corner was also intersecting another rectangle. It worked well enough and I am happy about it for now.

The following are some sketches and notes from my problem solving.

![Breakout sketch 0](breakout0.png)

![Breakout sketch 1](breakout1.png)


### Conway's Game of Life

I also made a Conway's Game of Life clone in Pygame. The public repo for it is [here](https://github.com/ClementineAccount/ConwayPygame)

![Conway Preview](conway.gif)

It took about four hours of total working time, although I spread it out over a week (an hour a day) instead of one shot. I also did it without looking up any other implementations too (I have never done Conway's before) and I am glad I didn't. It was really satisifying to just get the correct result by just following the rules 

It was fun to implement grid stuff. I was tempted to fall into the habit of pre-mature optimization by worrying about whether the Pygame's Rect class could handle a grid as well as the time complexity of accessing every grid and calculating their neighbors every tick but by making the rectangles big enough it was not an issue so far. 

#### Some notes

Here are some out of context I had taken while developing it

![Conway Notes 1](conway1.png)

![Conway Notes 2](conway2.png)

![Conway Notes 3](conway3.png)

I had already done these kind of 'mapping from global coordinates to local coordinate' transforms before many times in school, but I still felt like working them out quickly on paper as a sanity check. It is also a way to build a lifelong catalog of new notes stored on a cloud too, since I started using Obsidian a few months ago. 

Working out implementation from first principles is also a good way to further solidify an understanding too. Its a form of [active recall](https://en.wikipedia.org/wiki/Testing_effect) and exercises your brain. Way better than googling 'how to find 2D grid with 1D array' or looking at past code as the first resort. A solid understanding also helps someone be more flexible when the rules change (such as 3D arrays of voxels or when doing an isometric coordinate system (hints for what my current projects are).

![Conway Notes 4](conway4.png)

![Conway Notes 5](conway5.png)

Some notes when considering how to apply the rules on neighbours on my own. I did do a simple analysis of the time complexity of a neighbour and realise there's a potential for a problem, but I wanted to implement it myself first before I considered the optimisation.

#### Optimization

I also think that there's a good opportunity from this project to learn how to profile Python code better. Some suggestions that I had read was to use SnakeViz, which I will explore at a future time.

This is because there were a few lines of code during the neighbors checks for the cell state where I had to make educated guesses on how to better optimize them, but without profiling data they would remain as guesses rather than experiments. I suppose this could become its own full post in the future. Some of the things I will write about in that post would be the following:

- Clearing the list of new cell states every tick rather than creating a new one (I did implement this optimization and it lead to better performance, but without merits it could very well be a 'placebo' where a confirmation bias only notices the ticks where the framerate is higher)
- Using parallel concurrency with threads (however we need to be careful when allocating the memory for the cells that are to change states because it can be a race condition)
- Some other possible algorithmic optimization to reduce checks but I'd need to experiment and research more


### Pygame and Python thoughts

I noticed that even in these simple projects, the opportunities to create more universal tools and functions is there. It can involve simple stuff like refactoring the grid from Conway's Game of Life to be reusable outside of Conway, maybe even having a 'Has A' relationship rather than a 'Is A' one for Conway logic. I can also combine it with other grid projects like a Snake game.

However, due to the fact that these side projects may overlap more than expected, and the chance to make my own framework and engine from it naturally presenting itself, I decided that it would make more sense to focus on them in JavaScript rather than Python in the future. I am going to be playing around with the [PixiJS](https://pixijs.com/) renderer and would very likely move to using that for all future side projects of this nature.

I also found that while Pygame was easy to use, some abstractions from how the memory is laid out compared to working in C with SDL can feel a bit uncomfortable. I had a bit of issues understanding what type of data should do a `shallow copy` vs a `deep copy` in instances such as resizing the Conway Grid at runtime because it is less clear to me where the data is allocated and whether I was copying references or values. I am sure this is something that I could get used to over time as I work in Python more in the future though.

I will still do Python stuff but with more focus on scientific uses like from Anaconda rather than more real-time, interactive, visual stuff. I also rather split my time 90:10 between JavaScript and Python for the next few months too.


## Textbooks 

![Textbooks](textbook.jpg)

I also have been catching up on my reading and studying as I got a haul of used textbooks for free. My university library was giving them out and I came prepared to pick out some great finds, such as Dragon Book and Computer Systems: A Programmer's Perspective. I also got the famous Computer Graphics: Principles and Practice book. 

I have been setting aside time every evening to turn off my computer and simply study from reading, including doing some of the exercises from the math textbooks too. I find it's a great use of my evening time while reducing the exposure to blue light and improves the quality of my sleep. I will write more about what I had learned in a future weekly update post, however. So far I have just been catching up a lot on revising my Calculus 1 and 2, like derivatives and integral stuff.

# Conclusion

Writing a Weekly Post like this is kind of nice. I feel like it gives me a chance to talk about more things at an overview level without spending too much time on the depth (which means more time for studying and coding!). It also can act as a more useful record of my skill progression over time while being a source of accountability.

I will continue to write them over time. I guess in an ironic way it also makes this blog even more of a 'blog' in the traditional, pre-social media sense of the word too.

Next week's post would likely be about my experience with PixiJS as well as making new projects like expanded Conway grid or an isometric renderer. We'll see.