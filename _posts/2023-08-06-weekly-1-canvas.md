---
layout: post
title: 'Weekly 1: Canvas'
date: 2023-08-06 16:36 +0800
categories: [Blog, Weekly]
img_path: /assets/Weekly/Weekly1
toc: true

image:
  path: voxel.gif
  alt: Preview Image
---

This is the second post of the Weekly series I started last week. I changed a few plans to have a more focused scope.

I still have been relatively productive this week when it comes to my personal projects. This is a short overview of what I have been working on. Lately I have been exploring a few different things.

### Odin Project

The past few weeks I have been slowly progressing through The Odin Project for web development without getting overwhelmed with all the options there. I do a bit every other day at a comfortable pace at the moment. 

I get 'distracted' a ton though by also experimenting with my own web stuff after I learn a concept, I like to try and push my understanding. I guess you can't keep me fully trapped in [tutorial hell](https://www.linkedin.com/pulse/how-escape-tutorial-hell-ikechukwu-vincent/), which I suppose is a good thing.

The web ecosystem really confusing at the moment for me, since there's a lot of tech I am not familiar with such as 'NodeJS', 'Rollup', 'Webpack', 'Flask', 'Django', 'React', 'Vue', 'Electron', and... let's just stop there. I do understand some of these, for example I experimented with Electron to package a website as a standalone `.exe` and enjoyed that, but I noticed things started to get confusing when it comes to the `Webpack`, `Rollup` and `Parcel` such as 'why does it take 10 seconds to compile my TypeScript code here?'

The reason why I am choosing to do a simple course is that I want to build up core web concepts from first principles, starting from my basic HTML, CSS (I know the box model now) and JavaScript and slowly understanding each element of the tech stack one by one. I noticed when attempting to jump straight in I don't really have an understanding as to what each technology is meant to do and I had weirdly 'ritualistic' and superstitious ways of interacting with it (type this command in this way at this time to get it to magically work).

### HTML Canvas 

![Door projection gif](door.gif)

(All you need to do is divide by the z axis to start with)

Last week's post I mentioned being curious about PixiJS. Turns out, I don't need to touch that yet as the humble HTML Canvas that comes free with your computer has some nice functions for software rendering. We have [ImageData](https://developer.mozilla.org/en-US/docs/Web/API/ImageData) that lets you put pixels onto a canvas, and that's all you need to make a software raytracer or rasterizer. 

Even before that level of specification, you also have [lineTo()](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D/lineTo) which I have been using to revise and build my foundation for building perspective projection and transformation matrices without a library. No [glm](https://github.com/g-truc/glm) babysitting here. You got to remember what an Affine Transformation is and how a homogenous matrix represents that.

I was going to make that cube in the example rotate and spin, but then I realize that I computed those vertices in world space and not model space its relative pivot for rotation was the view's position rather than its local origin. An example of breaking TRS.

![Rotation gif](rotation.gif)

(That line that popped up was also a result of not clipping the z-axis as it approaches zero)

So I need to fix that first too. I did get sidetracked with other stuff which the rest of the post will discuss. After I am done with a wireframe 3D cube I'd need to implement the `ImageData` version instead as having access to pixel data would allow me to do perspective correct interpolation of uv coordinates for texturing when doing a rasterizer (as well as having a depth buffer).

## Voxels

I started working on rendering voxels for the first time on Thursday. Still need to make a bit more progress but I was able to apply what I had learned from last week with the Conway stuff onto a 3D thing. Going to experiment with the concept of a 3D Voxel.

![Voxels](voxel.gif)

To start with I wanted to see the performance limits if each voxel were to each have a single drawcall. I was surprised it got as far as a 25x25x25 grid which would be 15625 drawcalls. The first step of optimization is to use something like `glDrawElementsInstancedBaseVertexBaseInstance` to draw multiple instances of cubes and index their model/color/texture-atlases in the shaders.

Well actually the first step was making sure that each voxel was sharing the same index and vertex buffer, but I did that already.

## Plane Game

I decided to switch development from Plane Game to a different project, which is a successor of the Pixel Perfect game. Will write more about it next week once there is more development.

### Others

### Baby's First ECS

I also been experimenting with building my own ECS engine from scratch, inspired by a [reddit post by a Discord friend, the_Demongod](https://old.reddit.com/r/gameenginedevs/comments/jpy27u/where_to_learn_how_to_make_a_game_engine/gbjc73p/). I had worked with ECS engines before in undergraduate and am familiar with using the APIs my team made for our engine, as well as creating my own components and systems, but I had never made the actual entity myself. 

Both systems I worked with at school also use [RTTI](https://en.wikipedia.org/wiki/Run-time_type_information) but I wanted to explore options that did not have real-time reflection systems for the sake of performance and simplicity... or at least encounter the real situations where I'd want them despite the tradeoff. 

[Agner](https://www.agner.org/optimize/)'s optimization manuals suggest avoiding RTTI entirely, but of course we need to learn why with profiling and collecting data through benchmarking, otherwise premature optimization is just superstition.

Another thing to note is I like how the front-end of ECS is very similar to just regular Component-based architecture. An ECS engine's editor looks just like Unity's editor (the non DOTS version) from the gameplay scripting perspective.

#### Conclusion

There have been some other stuff I have been working on too, such as software isometric grid rendering without using projection (think SimCity 2000) or learning Rust, but I think this is enough for today's post. I rather write about what I have done rather than what I have been planning. Not as much to show for this week but it's setting things up slowly. I do think I spread myself out a bit thin between different interests but if there is no deadline I think it is ok. It just means that the individual projects get completed later but I get to learn more from the overlapping problem solving, such as the differences between writing an isometric grid software renderer that does not use a projection operation vs a perspective projection renderer.

I also have some ideas for some articles such as one on how to use the profiler for different ecosystems. I felt inspired by this Firefox post titled [2D Canvas Case Study](https://profiler.firefox.com/docs/#/./bunny) which showcases a case study on using the Firefox profiler to debug a software renderer. I want to make similar posts that act as a 'tutorial' for using profilers like [Tracy](https://github.com/wolfpld/tracy) or [SnakeViz](https://jiffyclub.github.io/snakeviz/) to profile and optimize cellar automata programs (like Conway's). I can also use the same post to discuss parallel programming using different languages, such as C, C++, Rust, Python and JavaScript, and whether there is a performance improvement when doing so for a software raytracer or a Conway's. So that's an article idea I have, but of course ideas are just ideas what matters is actually writing it down.



