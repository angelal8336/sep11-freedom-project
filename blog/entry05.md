# Entry 5
##### 5/6/24

### Process

The tool I used for my project was [KaboomJS](https://kaboomjs.com/). For the last few days, I have been trying to finish my MVP. For example, to finish my MVP, the main code I coded was the function `addMonster()`. `addMonster()` was a function that will drop a monster at a random position from the top of my screen. This sounds easy, but it was very difficult as I had to one, consider how to loop it forever/until condition is met, and two make the monster actually drop from a random position at a set interval. To begin, I first created the function, and added sprite monster, `pos()`, `area()`, and `body()` to it. From there I tried to give the monster a set position of (200, 200) like shown below:

```js
function addMonster(){
    add([
        sprite('monster'),
        pos(200, 200),
        area(),
        body(),
    ])
}
addMonster()
```

However, as you can imagine not only did it not spawn at a random place, it only ran once which was not the goal I wanted. However, since I wanted it at a RANDOM place, I tried to search up random on the kaboomJS website using ctrl f, and realize/remembered that Kaboom has a code that gets a random number for x to y. From there, I changed the set coordinate of my `pos()` and added `rand()` instead. The question now is between what numbers do I want the monster to spawn at. Well since I only wanted it to spawn at x between my canva size, I set `rand()` to 0 to 1280, and set my y equal to 0 since it will always spawn at the top of the screen. Below is the code I coded:

```js
function addMonster(){
    add([
        sprite('monster'),
        pos(rand(0, 1280), 0),
        area(),
        body(),
    ])
}
addMonster()
```

Like before, instead of working it broke my code. Apperently I cannot have three values within my `rand()`, and by adding 0 to 1280, I created three values, and a lot of syntax errors that stopped my ide from loading. From here, I had no idea what to do so I searched it up, and realized that I could of used `width()`, and `vec2()` to create what I wanted, so I did just that. Below is the code:


```js
function addMonster(){
    add([
        sprite('monster'),
        pos(rand(vec2(width(), 0))),
        area(),
        body(),
    ])
}
addMonster()
```

This code allowed my sprite to spawn at a random position of x while maintaining a y of 0, which is one part I wanted. However the problem now was how to make it spawn forever since this code only ran once. This is when I decided to try using my own loop. I put this code within a for loop and set i < 10. I was expecting it to work, but instead it crashed my browser. I kept trying to use the for loop in different ways, but no matter what I did it just did not work. I soon figured out that a function must be called in order for it to be used, and having a for loop the way I did it, didn't call my function at all. With this, I was stucked, but decided to ask mr mueller for help. He explained some concepts to me, and helped me code a bit until I figured out a way to loop my code forever without using a loop. Below is how I did it.


```js
function addMonster(){
    add([
        sprite('monster')
        pos(rand(vec2(width(), 0))),
        area(),
        body(),
    ])

    wait(1, () => {
        addMonster()
    })
}
```

I added a `wait()` code, and called my function inside that `wait()` so that not only just it delay my sprite from spawning, it always calls my function. This allowed my function to loop forever since it spawned a sprite, and then called `addMonster()`, and repeated this system. This code was in my opinion a genus method to keep my function running, but I wanted it to now run only a certain amount of times. To do this I tried using a for loop inside of my `wait()` to make it run a certain amount of times. However the loop inside my function broke my game, and gave me a system error that I had no idea how to fix, so I deleted the loop. Then I tried using an if statement that said if numMonster > 200 stop the code. However, I realized that numMonster wasn't define, so I created a variable called numMonster and set it equal to 0. To my surprise this method worked, but now I had to somehow make the variable increase whenever the function is called so that the loop will be able to stop when it hits 200. This was the easiest part of my code since all I needed was `numMonster++`. With that my function `addMonster()` was complete. Below is the code to the completed function:

```js
function addMonster(){
    add([
        sprite('monster'),
        pos(rand(vec2(width(),0))),
        area(),
        body(),
    ])

    wait(1, () => {
        numMonster++
        if(numMonster < 200) {
            addMonster()
        }
    })
}
```

The code above did exactly what I wanted which was to one, spawn the monster at random area and two, spawn it forever or until I wanted it to stop, which was the main code I needed for my game to work. However depsite that I still needed to code my player sprite so that whenever it touches a monster the game is over. To code this part of my MVP, I started with creating a scene of game over. To do this, I used the `scene()` code from kaboomJS, and added a `pos()`. Then I used `text()` to add the text of you lose to my screen, and scale it so that it will be big enough for the user to see like shown below:

```js
scene('lose', () =>{
    add([
        text('you lose'),
        pos(550, 400),
        scale(3),
    ])
})
```

However, when I ran the code my scene was not there, and nothing happened. I thought that I had made an mistake so I revised my scene code but instead it just made things even worst. After thinking for a while and scrolling through the kaboomJS page, I realized that `scene()` only makes the scene and in order to make it go to this scene you need to use `go()`. In other words, this scene will only run when I use the `go()` function. From this point, I realized that I needed a condition for the `go()` to be in, so upon thinking I realized that I needed to make my player sprite go to this scene whenever it collided with the monster. The reason for this is because the only way to lose is to touch the monster, so to do this, I used `onCollide()` function, and add the `go('lose')` within onCollide to make the user lose upon hitting the monster like shown below:


```js
player.onCollide('monster', (monster) => {
    go('lose')
})
```

This made it so that whenever player collides with monster, it goes to the scene describe by the code snip + 1 above. After this code was created, my MVP was basically done, since the game was able to end, and the user was able to play it. The only thing left for me to do was to change the pictures/sprites to the to the ones I wanted. In other words, I needed to replace my substitute sprite/images to the actual one I needed. After this was done, I was finally finished the MVP of my code. Here is the [link](../mygame/www/index.html/) to the final code.

In summary, I was able to not only code a function that allowed for a sprite to fall down at random area, I was also able to make the game end whenever the user failed to dodge the falling monster sprite.

### EDP

Just like the pervious blog, I am still on step 5 and 6 of the [Engineering design process](https://hstatsep.github.io/students/) which are to create my prototype, and test the prototype out.In a few days, I will begin step 7 of my EDP which is to revise and improve my code to make it go beyond MVP or to fix bugs I currently have. In a few weeks however, we will be on step 8 which is to communicate our results through presentation, and the SEP11 expo. As of now, my main focus to go beyond MVP, and make my game even better by adding sounds, and a scoring system with codes. To sum up, in terms of EDP, I will soon be on step 7 and 8 of my process which is improve, and communicate my game.

### Skills

The main skills I have improved on during this entry was the skill of creavity, and embracing failure. To me, creavity is having the ability to go outside of the box, and think of a alterative way to do something rather then just stick to the main road. Embracing failure is the ability to take mistakes not as mistakes but as courage to stand up and continue your work. In the entry, I have improved on both these skills since I had to think of ways to make my code work, and to keep going even when it was hard. For example I improved and worked on the skill of creavity and embracing failure, when I was coding my function `addMonster()`. Even though I tried so many ways to make it work such as having a loop or using `rand()`, my code always failed. However instead of giving up, I continued to code and tried my best to come up with another way to fulfilled my goal, which was to run the function forever or until a condition is met. I keep trying and tryng, and in the end I was able figure things out. Instead of using a loop or `rand(#, #)`, I decided to try an alternative way of going at it, which was using a `wait()` and calling my function inside the `wait()` while using conditionals, and using `vec2()` and `width()`. This allowed me to improve on both of the skills at the same time. Another example when I used these skills was while coding my scene. Even though the scene was not as difficult as `addMonster()`, there was one moment where I had no idea how to create a scene that has a text since I forgot that `text()` existed. Even though, I didn't use another way to create text, I still kept trying to figure things out until I remembered to use the `text()` function in kaboomJS to create an text. This moment allowed me to improve and use the skill of embracing failure since I refused to give up.

In summary, I have both used and improved on the skills of creavity and embracing failure, even if there are still a lot of room for improvement.


[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)