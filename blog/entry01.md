# Entry 1

11/13/23

## Process

After a long process, the tool I picked is called [KaboomJS](https://kaboomjs.com/), and the project I'm inventing is a parkour pixel game filled with obstacles such as mobs, or flying apples. To back track, we first need to start at the super beginning of the freedom project. At the start, we were tasked to put forward a few concepts; games, education websites, etc; that we would like to make using javascript. From these, I selected games as my theme, so I started to brainstorm the types of games I would like to create that would be doable and fun.  In the end I came up with two main ideas, parkour pixel, or a card game. Consequently, I ranked the tools for game creation, one being my first choice and three being my last. The list was as followed; [ImpactJS](https://impactjs.com/), [KaboomJS](https://kaboomjs.com/), and lastly [Phaser](https://phaser.io/). I then assigned one tool from the top 3 to each of my game ideas stated above that would best fit it. This was the beginning of my next step, which was tinkering.

To begin, I first started with ImpactJS by watching the game, and installing/getting started video in their documentation.  Then I moved onto trying to install it onto my PC, but failed to understand how to since there were alot of steps like needing to install PHP on windows, and komodo edit. However despite this, I kept on trying by learning the components or codes in [ImpactJS](https://impactjs.com/). Of course, I wasn't able to grasp how it worked even after more than 2 hours of trying. In turn, I dropped the idea of using [ImpactJS](https://impactjs.com/), and moved onto tinkering with [KaboomJS](https://kaboomjs.com/).

The first thing I did was of course look at the tutorial and figure out how to install it. After successfully installing it into my [IDE](cs50.dev), I started learning the basics of the tool. This being said, I looked at the game objections, and learned how to use `add()`, `make()`, `readd()`, `get()`, `destroy()`, and `destroyALL()`. For instance, I tried adding text onto the screen using `add()` and `make()` like this:

```js
add([ text(“hello”])
make([text(“hello”)]).
```
However the `make()` code did not work, and instead gave me a reference error/make not defined, so of course I kept on trying but in the end failed, which gave me an idea of asking for help on slack later on. After learning the basics, I learned the foundation of any game which was the sprites. First and foremost I looked at the example of how the website created a sprite using PNG files while using `add()`. Then I moved onto creating my own sprite using my friends' pictures by turning them into PNG files and downloading them into my IDE. This was the code I came up with

```js
add([sprite(“Ada”, pos(80, 40).
LoadSprite(“Ada”, “sprites/Ada1.PNG)
```

This code above, created an Ada sprite using the image I downloaded, which was exactly what I wanted. However, before reaching the correct code, I encountered Ada was not defined, and failed to load img of Ada1.PNG errors, which I fixed. Shortly after, I decided to partner up with Ada to make a parkour game (my idea), with incredible music (Ada’s idea) using [KaboomJS](https://kaboomjs.com/) (my tool), and [Earsketch](http://earsketch.gatech.edu/landing/#/) (Ada’s tool), because not only did it make both our projects better, it was a good opportunity to master collaboration. In other words, we found a common ground of wanting to create something that kids and adults would be interested in, since nowadays many games, and music are getting old, so creating something new would be nice.

## Engineering Design Process

We are still on step 1,2, and 3 of the Engineering Design Process, which is to define the problem, research the problem, and brainstorm possible solutions. In the near future, I hope to plan out and create a MVP prototype of my game. For this freedom project, the problem I chose to fight was the problem of boredom. These days games are getting old, and boring in my opinion so to solve it, I decided to create my own. I researched the different games out there that I don't play, and brainstormed what ideas would make my not so unique concept shine. Then I wrote down the ideas, and got prepared to soon, in about a few weeks start the next step of the process in the Engineering Design Process.

## Skills

The skills I used and improved on in this blog was the skill of creativity and embracing failure. Creativity to me is the ability to use your imagination to create something unique, while embracing failure is the spirit of never giving up. In this entry I have worked on these two skills by one, not giving up on trying to learn [impactJS](https://impactjs.com/) and [KaboomJS](https://kaboomjs.com/) even though I failed to understand it many times, and two, using my imaginations to brainstorm ideas of my game. For instance, even though kaboomJS gave me a lot of errors such as something not defined, I pushed through and kept on retrying instead of giving up on learning. In addition, brainstorming ideas such as the character or design of my game used a lot of creative juice, but I kept on going without ever losing hope. In conclusion, though both of these skills improved a ton, there is still a long way to go since I have plenty of room to grow.


[Next](entry02.md)

[Home](../README.md)
