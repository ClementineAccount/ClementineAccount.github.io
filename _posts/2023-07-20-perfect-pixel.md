---
layout: post
categories: [Projects, Student Projects]
title: Perfect Pixel
date: 2023-07-20 20:23 +0800

img_path: /assets/Projects/PixelPerfect
toc: false

image:
  path: preview.jpg
  alt: Perfect Pixel Gameplay

---

{% include embed/youtube.html id='9qxHauam3ZU' %}

[Perfect Pixel](https://games.digipen.edu/games/perfect-pixel) was a four person freshman student project made at DigiPen Singapore in C++. The project was created in two months during the year 2020. We used GLFW to handle the windowing and OpenGL to do rendering.

As a freshman, I created the rendering and animation engine for all sprites and pixel graphics in the game. The engine rendered the grid visualization using a single drawcall through modifying texels on an existing texture through the use of [glTexSubImage2D](https://registry.khronos.org/OpenGL-Refpages/gl4/html/glTexSubImage2D.xhtml) and used a separation of canvas scale and render scale for performance. I am quite proud of coming up with this method as a freshman. I also was responsible for adding a scrolling (movable) camera that offsets the rendered pixel based off a camera coordinate. Sprites were rendered as quads and had to have collision interaction with the pixel grid, which made the camera translation challenging at the time.

In addition to rendering, the game levels loaded using .bmp file formatting so external pixel editors could be used in-place of an in-engine editor. This was actually briefly mentioned in a [blog post](https://clementineaccount.github.io/posts/using-blender-to-edit-levels-in-my-3d-game-projects-instead-of-creating-a-level-editor/#using-paint-software-for-2d-level-editing) on this same site. 

