# Entry 2
##### 12/18/23

### process

Since writing entry 1, I have been working on learning all the componments of [KaboomJS](https://kaboomjs.com/) to the best I can. I would read the documents, try it's example if provided, then change parts of the code to see what happens. For instance, on 10/19/23, I tinkered with the following three componments, `pos()`, `scale()`, and `rotate()`. First I started with `pos()`, by setting, and changing the x and y coordinates to -, +, and decimal values to see what would happen. I realized that y values worked a little differently. Instead of moving up when the number is +, it moved down, which goes aganist the coordinate plane, and what I have always been told. After tinkering with `pos()`, I went to `scale()` and `rotate()`. For both, I did exactly the same thing as when tinkering with `pos()`, which was changing the numbers to see the result. For `scale()`, I initially set it to (1, 1), but eventually changed it to x = 2, x = -1, y = 2, y = -1, x = 0.5, and y = 0.5. From this, I learned that x values stretch my spirte from left to right, y values stretch from top to bottom, and values smaller than 1 shrinks the sprite. As for `rotate()`, I learned that + numbers move clockwise, - numbers move counterclockwise, and the position of the sprite is not constant. Fastfoward to 10/23/23 and 12/3/23 where I tinkered with `color()`, `opacity()`, `text()`, `size()`, `width()`, `font()`, `rect()`, `circle()`, and even made my own project using everything I learned so far. For `color()`, it was quite simple. All I did was change the R G B numbers to see what colors I would get. For instance, I once changed it to `color(20, 50, 10)`, which turned my sprite into a super super dark green color. Next up was `opacity()`, and `text()`. For opacity I wrote `opacity(100)` first in which nothing changed, then wrote `opacity(-100)` and the whole entire sprite disappear. Then for `text()` I made a hello world message, then proceed to learn `size()`, `width()`, and `font()` to make my text better. Here is the entirely of that code

```js
add([
	    text("Hello world", {
            size: 50
            width: 50
            font: "Times new romans"
		})
	])
```

After this long tinkering, I easily learn `rect()`, and `circle()` by changing the values like before to see what would happen. As expected the radius increased when the value went up, and the rectangle increased as width and height went up. However one thing I figured out was that - values do not work for these codes since the rectangle and circle wouldn't show up. Finally, we arrived at the masterpoint of all my tinkering so far. I created a project with every single piece of componments I learned so far. Here is the code for it,

```js

add([
    rect(200, 50),
    color(20, 50, 100),
    pos(100, 100),
    ])

    add([
    circle(100),
    color(140, 200, 5),
    opacity(0.7),
    pos(200, 300),
    ])

    add([
        pos(400, 100),
        scale(1, 1),
        rotate(50),
        text("Hello World", {
            size: 50,
            width: 300,
            font: "times new romans",
    }),
])

```

So basically what I did was mash up all the componments into one project, for example using `color()` and `opacity()`, for a circle created by `circle()`, or using `font()`, `scale()`, `rotate()`, `pos()` to make my `text()` unqiue. To sum it up, this was the end of my tinkering before writing this blog.


### Winterbreak goal

My goal during winterbreak is to learn the rest of the componment for [KaboomJS](https://kaboomjs.com/) which is around 16, and create a huge project with all the componment so that I can review them. Each day, I am hoping to learn 3 componment, which will take me about 6 days to complete it. Then for the rest of the break I will work on the project of using all the componments, while reviewing them for about 1 hour a day. While doing so, I will log them into my learning log, and write some notes for future entry's. The rest of the time will be spend on resting, and relaxing.

### Engineering Design Process

Currently we are on step 4 of the [Engineering Design Process](https://hstatsep.github.io/students/) which is to plan the best solution or in my case, plan the best way to create my game by learning how to use [KaboomJS](https://kaboomjs.com/). In about a month or so, my plan and hope is to create a prototype of the game. For this entry, I mainly focused on learning my componments, so that I can find a way to approach and plan the best solution to this huge project. For example, I learned how to use `scale()`, and `color()` to make my sprite more to my liking. Soon enough, we will be moving onto actually creating the game.

### Skills

The skills I used and improved on in this entry is how to google, and growth mindset. To me, how to google is the ability to find the things you want on google, and growth mindset is the ability to never give up even if things dont go well. In this entry I used both of these two skills by not giving up on learning my tool even when I don't understand and using google to help me learn my tool. For example, when I didn't understand how `text()` worked, instead of giving up I analyzed the example in [KaboomJS](https://kaboomjs.com/) over and over again, and then went onto google to search up a tutorial video explaining how `text()` worked. In addition to this, there were many times like when learning color and RGB, that I kept trying and googling until I finally understood how it worked. To sum it up, I have improved on both these skills, but still have room to grow.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)