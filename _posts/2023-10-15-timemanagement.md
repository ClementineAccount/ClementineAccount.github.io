---
layout: post
title: How you can effectively track your progress and your time... without stress
date: 2023-10-15 12:23 +0800

categories: [Blog, Articles]
img_path: /assets/blog/TimeManagement
toc: true

---

This post was originally written as a section for the blog post on [Game A Week 1], but I chose to move it to its own post as it got bigger, more detailed and more. I hope it can serve as a useful starting point for anyone hoping to better improve their ability to manage their time, reflect on work or communicate their workload to other people.

The post is written from the perspective of reflecting on the way I had spent my time working on a small game project from October 11th 2023 to October 15th 2023. 

I have been using the similar systems to track my time and progress since March 2023, refining them and improving them to this point. I chose the October 'Game A Week' project as the case study as it is the most recent success case of its use for a finished project.

Edit: Turns out a few similar points were also mentioned in the [Weekly 7 post too](https://clementineaccount.github.io/posts/weekly7/). Shows how useful it is that I wish to share it so often. 

## Time Tracking

Using the application [Toggl Track](https://toggl.com/), I took note of the intervals of time I had spent on the project, and on what kind of features. This allowed me to get a clear understanding not only of what I have done, but what I am currently capable of doing under certain time projections.

The following are some examples of the data gathered that is useful. 


![0](0.png)

The above screenshot is a report of how much time I had spent on each day for tasks under the category of 'Game A Week 1'. It reveals that I had started on Wednesday and had a slump on Friday, before making up for the lost time and polish on Saturday. A later section of this post will reflect on what caused such a slump. 

![1](1.png)

In addition to the overall elapsed time spent, I can track down what kind of tasks took up what kind of time. This is a screenshot of Saturday's tracked time, where I was most focused on the game. I was able to adjust my start and end times of full focused, pausing the timer when I was not working.

![2](2.png)

On Friday I can see that I did a bit of coding and also focused on coding for a project outside of this 'Game a Week' too. If I look at my journal, I can even see the type of tasks I was working on that day.

## Task Tracking

![3](3.png)

I use the application [Obsidian](https://obsidian.md/) to create markdown folders that are easy to organize. You can use any application you like, however, but this is what worked for me. In this application, I am able to sort my workload using [Hierarchical Outlines, as recommended by Masahiro Sakurai (Game Director for the famous Nintendo franchises, Kirby and Super Smash Brothers)](https://www.youtube.com/watch?v=ZzCfzwe23kw)

So for example, we can reflect on Friday's Journal and [Daily Scrum](https://www.kodeco.com/585-scrum-of-one-how-to-bring-scrum-into-your-one-person-operation), which is where I recorded a video of myself talking about the day's task. We can use this to get a glimpse into my thought patterns during that day.

![4](4.png)

So now we can view that in hindsight, Friday was actually a very productive day but was a straining one. I was focused debugging a critical performance bug, using the [Firefox Profiler](https://profiler.firefox.com/docs/#/./bunny) to narrow down why my collision detection was performing far worse than it should have been. In the end I fixed it on Saturday, identifying that I was creating callbacks in the [Update() loop](https://newdocs.phaser.io/docs/3.54.0/focus/Phaser.Scene-update) rather than the [Create() function](https://newdocs.phaser.io/docs/3.60.0/Phaser.Scenes.Events.CREATE).

These journals also act as a good way to remember concepts that I might have picked up from the project, such as how I organized my workflow to pipeline art from Krita to my game, or some quirks of the coding language I am working in. This allows me to cross reference more effectively with my previous work when I encounter similar problems or cases in the future.

![5](5.png)

I would save screenshot and links to relevant documentation or forum posts, including ensuring that the page was archived using the Internet by using an extension, to reduce Link Rot.

![6](6.png)


## Git Commits

I can also cross reference my progress with commit logs, which I can preview using something like Github Desktop.

![7](7.png)

## Daily Scrum and Kanban

The Daily Scrum is a useful way to force reflection by talking aloud about the progress. Preferably you'd want to do a direct video recording.

![8](8.png)

The way I do is it to write down a bulletin point list of plans and personal reflections, before recording a video discussing the same points similar to a standup meeting. The video is kept short, less than two minutes, before being attached to the page. 

In a bigger project, we would use Trello but for small Game A Weeks, we can also employ a simple kanban board to keep track of what is left to do.

![9](9.png)

For 'game a week', I actually am experimenting with separating things out by day since the timescale is so short. It has been useful so far. I had left behind the task of further polish as I wanted to just release.

In addition to a kanban board, I would write down a simple to-do list on paper as well, which can also cover some tasks that would not go on a board such as bug fixing or surprise tasks like balancing the game.

### Conclusions

Overall, through the use of simple time tracking and task tracking systems, I was able to get more useful information from a project beyond just my human memory and the final product. The combination of the tools [Toggl](https://toggl.com/) and [Obsidian](https://obsidian.md/) work together well in this regard, allowing a low overhead to maintain this system consistently. 

This makes the completion and progress of any project I work on have a higher gain on my own learning, without requiring much additional work on my part, while also keeping my focused on the task at hand. There might be some drawbacks through slowing down the task itself in the short term, but I believe the benefits of allowing easy accountability and reflection more than make up for it. 

It is a far more productive habit, if feeling the urge to alt-tab, to alt-tab back to these journals to write down what I am working on or what I am stuck on, than to look at Reddit or Youtube.

These systems also allow me to know exactly how much time was needed for tasks, or how much I really worked on rather than 'I felt like I was coding all day' or 'I didn't feel like I worked that hard, why do I feel so tired?' type of speculation. 

I highly recommend that everyone whom struggles with feelings of procrastination, slumps or feeling strained to meet deadlines, to try and develop systems to address them that suit their own personality and needs. While my own habits are successful for my case and can be used as a starting template, everyone is different and have different needs. 

I myself was only able to develop this system personalized for me after months of iteration and improvement and now I am very happy with it. No 'productivity life hacks' clickbait can appeal to me anymore.

