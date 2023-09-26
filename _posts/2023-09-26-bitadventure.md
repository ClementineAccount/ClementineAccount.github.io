---
layout: post
categories: [Projects, Game Jam Submissions]
title: "A retrospective for my game, Bit's Adventure"
date: 2023-09-26 20:40 +0800

img_path: /assets/Projects/BitAdventure
toc: true

image:
  path: gameplay.gif
  alt: Gameplay Preview
---
In 2020, a few months before I started my undergraduate education, I had developed a [small but finished game](https://clemboy.itch.io/bit-adventure) for [an online game jam which you can play here](https://itch.io/jam/godot-wild-jam-21). For context, game jams are game making competitions. This game was made with the [Godot game engine](https://en.wikipedia.org/wiki/Godot_(game_engine)). 

This post looks at what that game did well, what it could do better, and [why I end up choosing it as the basis for my first upcoming full commercial game project](https://clementineaccount.github.io/posts/weekly5), set to release on Steam by August 2024.

![Preview Image](preview.png)

## Background

My intentions for spending the week making this was more for fun, for my own learning and to challenge myself to make a game that could become a finalist. In the end, my game was ranked [1st place in the Fun category](https://itch.io/jam/godot-wild-jam-21/results/fun) and [9th place overall.](https://itch.io/jam/godot-wild-jam-21/rate/638544) This ranking was out of **88** total entries. 

The positive reception is a good learning point, as it highlights this game's ability to resonate with the audience. Even though it lost out a lot of scoring due to the amateur artstyle and not fitting the Theme of the competition, which was 'Connection', the core gameplay loop was accessible and fun enough to garner a lot of positive feedback. 

One of the challenges was making it a game that can be played with only two buttons, so I chose a mouse focused control scheme. For a platformer, this is quite unique as usually platformers are designed with controllers or keyboard only in mind. It hence unintentionally gave the game a unique selling point that stands out from other similar platformers by the control scheme alone.

In the following sections, we will analyze what the game has done well and what could be improved upon as learning points that I can consider in making the full release.

## Simple Self Review

### Instructions and Title Screen

The game's premise is very simple and easy to understand, where the video footage on the game's page already shows exactly what the player is meant to do. 

Despite that, I quite like that the written instructions on the title screen still emphasizes how simple the game is.

![instructions screenshot](instructions.png)

The choice of including icons representing the game objects in the title, rather than referring to them by names, allow the player to easily understand what they need to do in the actual game.

Regardless, even if no instructions were included, the early level design of the first level still teaches you how to play it.

### Early Level Design

The introduction levels were quite strong, especially the first one. The only instruction given is a text indicating the game's controls. 

![first level](first_level.png)


It states to simply use the mouse to play. It leaves it vague not to overwhelm the player with too many technicalities straight up, while giving room for experimentation. 

The player starts off in a very safe column, surrounded by walls. This teaches them that these walls on the side are safe to touch, and the ball would bounce off them. It also gives a satisfying 'ping pong' effect of the ball bouncing back and forth between the walls if the player does hit the wall.

The key is positioned right above spikes so that players would have a chance of encountering that those are the hazards that force them to reset the stage. It also shows the game's basic challenge and hook straight up: "Can you catch the keys without getting caught in the spikes?"

This is a relatively simple game so I will move onto discussing the third level which I think was quite flawed.

## The Third Level is not as good

![third level](third_level.png)

The first two levels prior to this point were quite simple but I feel the difficulty jumps up too quickly between the second and third level. While designing this level, I think I wanted to subtly introduce to the player that it was ok to use the 'slow down time' mechanic when you are aiming your shot to gently ease their way down the spikes. I also wanted to encourage the player to use the teleporter to return back to the entrance rather than fly back.

I think, however, this level was too early in the progression and tried to teach two lessons at once. In the full game, we will need to do better pacing.

## Hooks

The hook of playing the game under a certain completion time in order to unlock harder levels is good. 

![main menu](main_menu.png)

![unlock_hard](unlock_hard.png)

It encourages players who enjoy the gameplay loop and are skilled at the game to get better at it in order to play faster, while the reward is not relevant to players who are still struggling with the basic levels. 

In my view, this is a strong way to frame a reward to incentives players to try the game again when they are good but it also doesn't 'punish' the players who are less skilled at the game, compared to more traditional grading system.

It also gives a 'goal' right from the very beginning of the title screen to work towards even for such a simple game, as to why bother completing the Normal Levels first. 

A player's curiosity is already activated as they would already have thoughts like 'What is hard mode? Is it really that difficult to unlock? Are the levels much tougher?' even before they hit the start button. 

Since the game does not have a strong story, this is a good alternative 'hook' to still encourage them to try the game and complete all the levels.

## Teleporter

The teleporter mechanic is a good idea but the execution could be better. It is too easy to accidentally teleport twice if you are playing with a touchpad. 

One way I could've mitigated this was by using a 'weapon wheel' like mechanic, [which one of my earlier games had done for shape shifting](https://clemboy.itch.io/super-shape-shift). If the player can select to place a teleporter and activate it through a menu like this, holding down the right-mouse button it would feel much more smooth.


![wheel](wheel.png)

## Should we adapt it to a full release?

### The positives 

#### It is fun

As discussed earlier, the game's concept has some good design and hooks that guarantee that it has fun and appealing core gameplay. The game jam version acts as working 'proof of concept' prototype of design that gave us useful information on how the game is fun, and that people do enjoy it.

Even outside of playtesting, I myself still enjoy playing the game just for fun and completing the levels. 

#### It has good accessibility for the genre

The controls involving only a mouse makes it a good 'pick up and play' game for people on the computer. This gives it both a focus on the target platform, which are desktop and laptop computers, as well as a unique identity among other platformers of a similar genre. 

Other skill-based platformers will target a gamepad as the genre expectation, so this also helps the game stand out. Usually, mouse-only game controlling a ball is contextualized as a 'golfing' or 'pool' game in theming too so the framing as a more traditional platformer may help appeal to people who do not like the sports theming.

#### The Scope is very manageable and small

We know that the scope is small because I had already made the game before. This reduces a lot of the design risks of whether the game is fun straight out, saving potential months of playtesting and redesigning the core concept.

The [minimum viable product](https://en.wikipedia.org/wiki/Minimum_viable_product) of this game of single screen challenge rooms is already appealing, fun and proven. 

Despite this, there is still potential for growth of the concept, such as moving camera or scrolling levels. Since the core foundation is already good, adding more layers onto it and experimenting with how the core concept can be tested is less risky, as if the experimental designs do not work we already can fall back to a well proven framework.

## The negatives

### The unique selling point is not very innovative 

The core concept of a platformer where you control and slingshot a ball around freely is quite novel and not very common, but it is also not a strong hook on its own. 

There is no real 'wow' factor that can grab the audience's attention when browsing a storefront or looking through other platformers. It also is unlikely to capture the attention of judges for competitions on the gameplay loop alone, even if well executed, because it is quite derivative of well established design.

The mitigation for this means that the game's marketing is forced to have to rely on the game's arts direction and aesthetic in order to capture the initial attention. The way I intend to do this is focusing on experimenting with raster scanline special effects and allocating a healthy amount of development time for polishing.

## So should I make it? Yes

The game Bit's Adventure is just fun. I recommend that everyone reading the post still play it. Using this as the basis for my first commercial game would be wise due to its very reasonable scope.

I also have to keep in mind that the platforming genre is quite mainstream and crowded, so it is unlikely for the game to stand out. This is okay if I budget my development costs accordingly to have a very modest return, aiming to break even. 

By having an expectation of this game as my first commercial project and entry as a back catalog, I also can set realistic expectations that all I need to focus on is making a quality product and what I will learn from the process of production from start to finish, even if it does not make waves. 

Having a small but good quality finished game also adds a lot of credibility to my back catalog as an independent creator, which can in turn justify taking risks for more ambitious and innovative but potentially higher rewarding projects... or help me discover a niche target demographic to cater to.

A commercial project is also the perfect 'springboard' for my own custom 2D game engine that is being developed for it. This engine can grow over the decades to make focused games in a workflow that allows me to be very efficient, while having features that are harder to replicate with generalized game engines like Godot or Unity (allowing those games to stand out). 

By considering this project as the first in a longer span lineage of games, it justifies its development cycle and low cost quite well despite its lack of potential for strong success in a marketing perspective.