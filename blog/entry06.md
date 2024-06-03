# Entry 6
##### 6/2/24
### Context

Me and Ada created a game using [Kaboom](https://kaboomjs.com/) that testes out our reflexes while reducing stress. We created a game called dodgers where you had to dodge the falling monster while trying to collect as many coins as possible. In the game, there is a bean sprite which is the player, a egg sprite which is the monster and lastly a coin sprite. To move, you use the left and right arrow keys, and to jump you use the space bar. When you collect coins, and game over you have sound effects. This game is created with Kaboomjs and Earsketch.

When we finished creating this game, we were able to present it in the sep11 expo, and in class presentation.

### Process for beyond MVP

After finishing my minimum viable product for my kaboom game, I had a few days for beyond MVP before we started class presentation/expo. For beyond MVP I decided to add:

1. Coins falling; whenever you touch a coin, you gain one score and the code disappears
2. Additional sounds; coin collecting and game over sound

To code the coin falling, I basically just reused my `Addmonster()` function, and instead of having the monster sprite spawn, it would be a coin sprite. I deleted the if statements for the variable Nummonster since I didn't need to set a limit to coin, and changed the wait time to be slower, like shown below:

```js
function addCoin(){
    add([
        sprite('coin'),
        pos(rand(vec2(width(),0))),
        body(),
        area(),
        'coin',
    ])

    wait(3,() =>{
        addCoin();
    })
}
```

For the score board I created an variable called score, and increased that variable by one while adding it to the screen using `text()`, whenever the coin collides with the sprite. To make the coin disapear all I did was add `destory()` to the collide function like shown below:

```js

var score = 0;

player.onCollide("coin", (coin) => {
    score++
    add([
        text(score),
        pos(200+x, 200),
        scale(2),
    ])
    coin.destory()
})

```

When coin falling was done, I wanted to add more sound effects to my game to make it more "fun" and creative. To do this, I asked ada to create what she thought a coin collecting and game over sound sounded like using Earsketch. Then after she was done, she downloaded the music into an mp, and emailed it to me so that I can import it into my IDE file, and then my game using `loadSound()`, and `play()` like shown below:

```js

loadSound("music1", "Sounds/JoyMusic.mp3")
loadSound("music2", "Sounds/coin.mp3")
loadSound("music3", "Sounds/fail.mp3")

player.onCollide("monster", (monster) => {
    play("music1", {
        volume: 0.3,
    })
    play("music3", {
        volume: 0.8,
    })
})

player.onCollide("coin", (coin) => {
    play("music2", {
        volume: 0.8,
    })
})
```

Since we only had a few days to add any beyond MVP ideas, we only added some small and basic stuff that we already knew how to do. In addition, we took some of our peers idea from the walk around and incorpated it with our own ideas to come up with these beyond MVP, so thank you to them.

### Takeaways from class presentation

After our beyond MVP was done, we started to create [slides](https://docs.google.com/presentation/d/1rB_4k91AYzV5LOHKlTsBIXt-eBn3NQzPUS3SnhKBGOg/edit) to present our project to our class that explains our challenges, and how we coded our project. From the class presentations, I learned and had some takeaways such as:

1. Communication is key. Me and ada had to be on discord calls every night before the presentation. We had to organize our slides, and lines so we know which person is saying what. We gave feedbacks to each other, and went over issues we thought needed to be fix. Together we made sure everything was well planned, and each of us knew which part with ours, so when the day comes we are ready. In addition, we had to practice our speeches over and over again until we understood and memorized the general format, so we could wing it just in case. We communicated with each other our needs, and ideas which made our presentation a success. Without communication, we would have been lost, and failed.

2. Always check the verison when your using an application such as Kaboom. When one of my classmates were talking about their challenges, I realized that we had the same issue of using `solid()`, and getting an error saying solid was undefined. Before their presentation, I had no idea why it didn't work since kaboomjs's example used it. However, when they explained that it was due to the fact that solid was removed from the newest verison, I understood that the kaboom I was using was old. This made me understand that I need to check the versions of app's or websites before I use them.

3. Practice makes perfect. Me and Ada both had to practice our lines to the presentation and the elevator pitch so that we were ready to explain to our class, and to the judges what we made. Both of us had to practice more than 10 times so that we can memorized what we wanted to say. The first time we practiced our presentation, we made many mistakes, and pauses that resulted in our time being 15 minutes. However, we kept on practicing, and the last time we practiced we had a time of just under 10 minutes, which was a huge improvement, since it showed us that we were more confident.

### Takeaways from Expo

After participating in the expo, and giving our [elevator pitch](https://docs.google.com/document/d/1fv9_xe7SCYjQU7sPjbECQIfCxmS7lNPs7SY7PmDEbWQ/edit) to the judges I had some takeaways:

1. Having an short but clear elevator pitch is important. I realized that having an elevator pitch is important since it gives people an idea on what you made, and how you made it while giving them reasons to be more engaged in your project. It's the first impression that you give to people about your project which is important, since it will decide whether they want to look at it or not. The moment, I understood this takeaway is when I was giving my own pitch, and observing other's. I noticed that the judges and my peers were interested in projects that had an good pitch, and not ones that didn't explain things correctly. In addition, when they came to my project, I realized that they were very engaged with my project after my pitch was done, which also made me realized this takeaway

2. Your opinion is different from others. I initial thought my project was not fun, since it didn't really have much to it unlike some other projects. However, when the judges, and classmates played my game I could truely see they were having fun, since they were screaming and laughing when they couldn't dodge the monster. This made me happy, and I realized that just because you think a certain way, doesn't mean someone else thinks that way too.

3. The end result is different than the starting/middle point. Though I had many challenges along the way, I was still able to produce a project. During the year, I thought that I wouldnt be able to finish due to my stuggles of not understanding the documents, and codes. However, when the expo hit, I had a sense of proudness knowing that I was able to finish my product, and even present it. Even though, my code didn't look complete before the expo, I was able to get it done.

### Engineering design process

We are currently on the last step of the [Engineering Design Process](https://hstatsep.github.io/students/) which is to communicate the results through the class presenatations and expo. After the presenting, we will be back at step 7, which is to improve as needed, since we will be able to get some feedback from our peers and teachers. However, after the summer, the whole EDP steps will be restarted, meaning we will be on step 1, which is to define the problem since we will start a new freedom project. My main focus right now is to explain my project to my peers around me, and showcase off what I had learned and created for a year.

### Skills

The skills I used and improved on is the skill of communication and time management. Communication is the ability to be able to convey your ideas to your partner, and peers, while time management is the ability to finish your task on time. In this blog, I improved most on communication because I had to use it for almost everything. For example, I had to talk to my partner Ada every night through discord to discuss over what to change/improve/make. In addition, we had to communicate in order to practice our presentation, and elevator pitch over and over again until we felt comfortable. We also had to present our project to the class, and to the students, and judges during the sep11 expo. I had to explain to them what I created, how I created it, and what challenges/takeaways I had. In addition, I had to explain step by step of my codes, and showcase my final product to everyone. As for time management, I had to finish my slides, and elevator pitch in time before the expo and class presentation started. In other terms, I had to manage my time in a way where I was able to finish sep work on time while completing work for other classes. In summary, I have used and improved on these skills the most, but I still have room to grow.


[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)