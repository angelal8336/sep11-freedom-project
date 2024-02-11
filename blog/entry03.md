# Entry 3


##### 2/5/24

### Process

 For the past few month, we have continued learning our tool, which in my case was  [KaboomJS](https://kaboomjs.com/). The [last entry](entry02.md) left me half way done with the conponment list, so in this entry I started learning the codes that would be helpful. For instance on 12/10/23, I tried to learn how to use `outline()`, and `body()`. To learn `outline(w, c)`, I first tried to write `outline(6, BLUE)` to give my kaboom sprite an outline of width 6 and color blue. Then I tried changing the values of the width to multiple numbers like 1, 2, and 100. As for the color, I tried using rgb values instead of key words to get a specific color. However, to my suprise, non of tinkering actually worked, meaning there was no outline on my sprite no matter what I tried, which left me confused. After a while of thinking, I decided to try the outline on a shape instead of an sprite, so I choose a rectangle. To my suprise the rectangle had an outline of the color and width I choose, which made me wonder if it only worked on a shape. But non the less I figured it out.

Here are two of the code that failed:

```js
    add([
        sprite("Kaboom"),
        loadSprite("Kaboom", "sprites/KaboomSprite.PNG"),
        outline(200, 50,20,30),
    ])
```
```js
    add([
        sprite("Kaboom"),
        loadSprite("Kaboom", "sprites/KaboomSprite.PNG"),
        outline(6, BLUE),
    ])
```
Here is the code that worked:

```js
    add([
			    rect(100, 50),
			    outline(2, BLUE),
		    ])
```

Moving on, the most important learning of the day was learning how to use `body()`. At first, I tried just adding `body()` to my sprite to see if it did anything. However, it gave me an error instead, so I went on kaboomjs website to see what I was missing. By doing so, I figured out that `body()` must come with `area()` and `pos()`, so I added thoses to my sprite. Now I was expecting, it to do something like fall due to gravity but nothing happened even though I had no error, which made me confused. I tried searching it up but ultimately I couldn't find anything that would allow my sprite to fall even though the kaboom website said `body()` makes sprite respond to gravity, so I decided to call it a day and ask about it later on.

A few weeks later, on 1/7/24, 1/14/24, 1/29/24, and 2/4/24 I learned the codes that were most important to my game which included `addLevel()`, `getGravity`, `setGravity` , `DoubleJump`, `solid`, `moveTo`, `OnkeyPress`, `.jump`, and much more. To start off, I first tried learning again how to make my sprite respond to gravity. I added `body()` componment along with `area()` and `pos()` (learned this before), so that I can add gravity. Just like before there was no gravity, so once again, I went to youtube to try and search up how to get a gravity. However, no video actually explained how it worked, so with all hope lost I went through the whole kaboom document to find something that will allow gravity. That is when I discovered `getGravity` and `setGravity`. When I added `setGravity(100)`, and `getGravity()` to my sprite, it started to fall. I then wondered what would happen if `body()` wasn't added, so I deleted it. Like expected gravity did not work without `body()`, so I readded it into my code.

Below is the code that worked:

```js

    setGravity(1600)

    const bean = add([
                sprite("bean"),
                pos(200, 200),
                body(),
                area(),
                getGravity(),
            ])

```

After learning this, I then learned how to jump on space using `.jump` and `OnKeyPress`. This process was not easy at all since the syntax in the website really confused me. I had no idea where to start so I decided to just copy the example into my code. I was expecting it to work, but for some reason it gave me an error, which confused me even more. However, I still decided to give it a go, so before starting I watched a [youtube video]( https://www.youtube.com/watch?v=n-q0pKGhxyw&t=248s), and even went to kaboom's github to see their library to understand it better. Nonetheless, I was still as confused as before, so I sat there and tried for 30-60 minute staight trying to get it to work.

Below is one of the code that didn't work:

```js
    onKeyPress("space", {
            "space": bean.jump(),
            })
```

After trying for about a good 15 more minute I discovered that the example code now worked in my ide, so once again I decided to follow the exact syntax of it like before. This time, the syntax was corrcect and I finally got it to work. This whole time, I was struggling with the syntax of the code but now looking back it was the one I wrote before but for some reason it did not work, and it looked wrong, so I gave up on it. As for the `.jump` it was very easy to learn since all I needed to do was add `.jump` to my sprite name inside the `onPressKey` to get it to work. While tinkering with all this, I also figured out that you need gravity in order for the sprite to be able to jump. I figured this out, by removing gravity and readding it to see what it would do to my code. In additon, during that time I tried to use `.doubleJump(5)` and `.doubleJump(2)` to get my sprite to only be able to jump that amount of times, but it did not work because it was undefined. However, instead of giving up, I tried putting `doublejump()` in the const and `.doublejump in the `onKeyPress`, which made it so that my sprite was only able to jump one time.

Below is the code that works:

```js

setGravity(100)

onKeyPress("space", () => {
         bean.jump()
     })

```

```js

    setGravity(100)

    const bean = add([
            sprite("bean"),
            pos(200, 200),
            body(),
            area(),
            doubleJump(),

        ])

    onKeyPress("space", () => {
             bean.doublejump()
        })

```

On that same day after figuring thoses things out, I used `moveTo` to get my sprite to move to a certain `pos()` on the screen. This code was important but it was not difficult to learn since all I needed to was put a coordinate inside the (), and attach it to a sprite just like `.jump`.

Fast forward to a week later, I learned how to use `addLevel()`, which was the most important code I would need for my game to work. Just like before, I first started by remembering how to format the syntax. I wrote exact what the example showed, but changed the symbol and sprite to what I defined. For instance, instead of putting % I used = for all my tiles, and changed the sprite to my bean sprite. However, even though I thought I have defined my sprite and symbol, I still got an error of symbol and sprite cannot be defined. I tried using the example code and revising my syntax just in case, and even tried redefining my sprite and symbol on top, but it still did not work. In addition, I tried using '' instead of "" to see if it made a difference. However most of the time it "gave me a Level symbol def must be a function returning a componment list." error, in which I did not understand. At times, it would even give me an `solid()` is not defined whenever I added an solid componment into my code to make the floor not passable. After trying for a long time, I felt hopeless and decided to rest for a while. After a while, I came back determined to figure it out, and this time it actually worked. Honestly speaking I have no idea what I did but for some reason my code worked.

Here is the code that worked:

```js
     addLevel([
            "                                                       ",
            "                                                       ",
            "      =       =      =            =            =       ",
            "                                                       ",
            "                                                       ",
            "       =         =               =            =        ",
            "                                                       ",
            " ====================================================  ",
        ], {
            tileWidth: 20,
            tileHeight: 30,
            tiles: {
                "=": () =>  [
                    sprite("bean"),
                    pos(0, 400),
                    area(),
                ]
            }
        })

```


Another week passes and I was stuck trying to figure out how to defind `solid()` in order to make my floor solid. I gave `solid()` an number inside the (), tired to set solid() equal to something, and even put solid inside an add instead of an tile. But no matter what I tried it was always undefined. However, when I was about to quit, my friend ada came in cutch and helped me to realize that instead of putting solid you needed to put `body({ isStatic: true })`, which makes the body solid. When I realized this everything clicked, and I tried making an `addLevel` with a solid floor, as well as a sprite solid.

This is what I came up with:

``` js
 addLevel([
            "                                                       ",
            "                                                       ",
            "                                                       ",
            "                                                       ",
            "                                                       ",
            "                                                       ",
            "                                                       ",
            " ============================================== ",
        ], {
            tileWidth: 20,
            tileHeight: 30,
            tiles: {
                "=": () =>  [
                    sprite("floor"),
                    pos(0, 400),
                    body({ isStatic: true }),
                    area(),
                ]
            }
        })

```

There was other code I learned such as `anchor`, but thoses were easy to understand, and wasn't that important so I decided not to include them in this entry. With that, the next step in learning is to learn the events of kaboomjs like `onCollide()` so that I am able to start making enemies, and obstacle in my game for the user to overcome.

### Enginnering design process

Like the last entry, we are still on step 4 of [Engineering Design Process](https://hstatsep.github.io/students/), which is to plan the best way to create my game. In the near future, I hope to start actually creating my game, and testing it out to see if it works and needs improvements. As of now though, my next step is to finish learning the componment, and events needed to create my parkour game. Speaking of learning, in this entry I mainly focused on planning (step 4 of EDP), or in other words learning kaboomjs. Like stated before, soon we will start to move onto step 5, 6, and 7 of the EDP which are to create, test and improve on our prototype.

### Skills

In this entry, the skills I improved and used were growth mindset, and How to learn. Growth mindset is the spirit of not giving up, while how to learn is the skill to learn on your own. As for me, I improved on these skills by using it over and over again in entry. For instance, there were many times such as learning `addLevel()` where I was about to give up since it was that confusing. However despite feeling that way, I still continued trying and pushing through the feeling of giving up which eventually lead to suceess. In other words, I had a growth mindset and the ability to learn on my own that allowed me to be able to learn many of the conponment including `.jump`, and `onKeyPress`. Another example, of me improving on my skills were when I was learning how to use all the componment like `setGravity`. I was able to learn this on my own without much help and struggling through it without giving up on learning. This shows that I was using and improving on how to learn, and growth mindset. Even though, I have a long way to go in improving on these skills, this whole entry was me using the skills I mention above.

### Next step

I'm planning to learn how to use all the events like `onLoading()`, `onError()`, and `onCollide()` to make my game more interactable to the user. In other terms, I would like to basically learn it so that I can start making my game.


[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
