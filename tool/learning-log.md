# Tool Learning Log

Tool: **Kaboom**

Project: **Parkour game**

---

## 10/29/23:

#### tinkered and learned

* watched parts of some videos on what kaboom can make
    * https://www.youtube.com/watch?v=jcoiEpzD3yc

* Set up my kaboom server
    * Downloaded the NPM mygame into repo
    * Pasted the CDN into my html file in mygame repo

* tinkered with start kaboom example
    * Deleted kaboom() and found out the game won't start without it
    * Tried to delete a sprite and the game didn't load
    * Changed the position of bean, and found that + x moves right, and + y moves down.
    * Changed rotation but it did nothing

* add() adds componment together such as the nose, heads, position, text, etc (it's like building with lego), and returns it.
     * anything can be a componment
     * tinkered by creating a text message using add()
        * add([
            text("hello")
        ])

* make()is like add() but does not return it
    * when I wrote `make([text("hello")])` it gave me an referenceerror/make not defined
        After trying for a while it's still an error so later on I'm going to ask for help on this


####  Next step
* Learn and tinker with the rest of game obj such as `readd()`, `get()`, `destory()`, `destroyAll()`.



## 11/5/23

#### tinkered and learned

* Readd() = removes/add game object
* Get() = group/get ALL objects with a tag label
* Destory() = remove objects
    * tinkered by trying the example code, and making my own verison of it so that the bean spirt upon touch will be destroy
* DestoryALL() = remove all objects with a tag

* Tried creating my own sprite
    * made my friend into a sprite by using `loadsprite`, `add()` and a saved picture
        * problem - The sprite was way too big (covered half my screen)
    * added two sprites into on page
        * at first it didnt work even through everything was typed correctly i think but after copying the example and changing the image/tag name it worked

* Tried using the sprite I created to destroy another sprite
    * first try it gave me Ada was not defined
    * second try it gave me "failed to load img of Ada1.PNG"
    * Next time ask for help on slack about this code
        * ```
        loadSprite("linnlett", "sprites/linnlettcrop1.PNG")

        add([
    	    sprite("linnlett"),
    	    pos(80, 40),
		])

		loadSprite("Ada", "sprites/Ada1.PNG")

		add([
    	    sprite("Ada"),
    	    pos(80, 40),
		])

		Ada.onCollide("linnlett", (linnlett) => {
    	    destroy(linnlett)
        })

        ```
#### next step
* Learn to change the properties of a sprite




<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->


## 10/19/23

#### learned/tinkered

* Learned how to use `pos()`
    * Tried giving my ada sprite different positions (x, y) to see where it would go
        * I changed x from 100 to 200, and it moved my sprite right.
        * I changed y from 100 to 300, and it moved my sprite down, and not up??

    * Tried using negative values for x, and y
        * I changed x from 100 to -100, and it moved sprite left
        * I change y from 100 to -100, and it moved sprite up??

    * Tried decimal point values
        * When X was 0.50 it moved left
        * When Y was 0.99 it moved up

What I learned is that + x value moves right and + y value moves down. To move the opposite direction use decimal or - values.
Side note: + y IS MOVING DOWN, and - y is moving UP

* Learned/tinkered with `scale()`

    * Enlarging sprite tinkering
        * Set scale to (1, 1) intally
        * Changed x to 2, and it strenched my sprite from left to right
        * Change x back to 1, and y to 2, resulting in strenching of my sprite from top to bottom
        * Change both x and y to 2, which resulted in a scale up by 2, keeping all the dimeondiol the "same"
        * Return x and y value to 1, and changed x to be -1, which made my sprite flip or reflect over the y axis
        * Returned x to 1, and changed y to -1, which made sprite reflect over the x axis
        * Changed both x and y to -1, which made sprite reflect over x and y axis

    * Shrinking sprite tinkering
        * Tried using decimal point as values, and it shrink my sprite

What I learned is that decimal point shrink my sprite while whole numbers enlarged my sprite. Negative values flip/ reflect over a x or/and y axis

* Learned how to use `rotate()`

    * Rotated my sprite by 5, 10, 20, 40, and 100 degree
        * Found out that the sprite positions moves or in other terms doesnt rotate at the same spot (moves around)
        * Rotates clockwise

    * Rotated my sprite by -5, -10, -40, and -100 degree
        * Found out that the sprite moves
        * Rotates counterclockwise

    * Rotated my sprite by decimal points
        * Barely rotates

What I learned is that + value rotate clockwise, and - value rotate counterclockwise. In addition when rotating the sprite is not at a fixed position.


## 10/23/23

* Learned how to use `color(R,G,B)`

    * Changed R value to 20, G value to 50, and B value to 10
        * Sprite color became a super super dark green color

    * Change R to 0, G to 0, and B to 0
        * Sprite color became black

    * Changed R to 100, G to 100, and B to 100
        * Sprite color became dark pee or yellow color

    * Tried to learn how RGB colors work, but failed to understand so planning to try again next week

    * Negative values changes the color (I don't know why)

What I learned is that the values of RedGreenBlue is hard to understand and each value determines the amount of red, green or blue that is in the color

* Learned how to use `opacity(#)`

    * Opacity is how transparent it is

    * Intally set opacity to 0, and then changed it to 5, and 100
        * Nothing changed

    * Changed opacity to a negative value (-100, -1, and -50)
        * The sprite disapper or became transparent

    * Changed opacity to a decimal value (0.80, and 0.50)
        * 0.80 opacity made sprite a little transparent
        * 0.50 opacity made the sprite super transparent

What I learned is that + values of opacity does nothing, decimal values make the sprite/element more transparent, and a negative values makes sprite disapper.

* Learned how to use `text()`
* added a hello world text to my game using this code:

 ```js
add([
			text("Hello world", {

			})
		])

```

* Learned how to use size, width, align, font with `text()`

    * `Size:`
        * Changed size to 100
            * Size of hello world enlarged

        * Changed size to negative 10, and 0.99
            * Hello world disappered

    * `Width:`
        * Changed width to 50 and 300
            * At 50 width the text wrapped around it's self
            * At 300 width the text didn't
        * The width code sets a range for the text
            * If the text goes pass the width, the text will wrap around it's self

    * `font:`
        * Changed font to times new roman

    * The text notation is text("Text", {size:, width:, etc})

What I learned is that to write a text you use `text()`, and to change the properties of the text you can use `size:`, `width`, etc.



## 12/3/23

* Learned how to use rect(w, h) // w is width, and h is height
    * Set w to 500, and h to 500
        * the rectangle/square took up around 1/3 of the screen
    * Set w to 1000, and h to 1000 (trying to find the width, and height of the whole screen)
        * the height filled up the whole screen, but the width had about 1/3 more to go
    * The height of whole screen is about 750, while the width is about 1540.
    * Tried setting W and H to -#, but rectangle didnt show up
        * W and H can only be a +#

* Learned how to use circle(r) // r = radius
    * Set radius to different #
    * Changed the color of the circle using what I learned before (color(20, 30, 40))
        * Circle became black or navy blue
    * Tried scaling up the circle using (scale(3, 1))
        * It turned my circle into a oval
        * You can use scale to change the shape

* MADE SOMETHING WITH EVERYTHING I LEARNED BEFORE AND NOW
    * CODE IS IN THE mygame, www, index.html.


## 12/10/23

* Learned how to use `outline(w, c)` // w = width, c = color
    * applied outline color to a newly imported sprite
        * ```
            Code: add([
			    sprite("Kaboom"),
			    loadSprite("Kaboom", "sprites/KaboomSprite.PNG"),
			    outline(200, 50,20,30),
		    ])
            ```
                * My sprite loaded but no outline.
        * Tried giving sprite a position, as well
            * Didnt work
        * Question: Why isnt my code working, and how do i use `outline()`,
        * Instead of putting rbg numbers as color, tried putting words like CYAN
            * Didnt work
        * Next step: Ask Slack my question

* Learned how to use `body()`
    * Gave my kaboom sprite a `body()`, `pos()`, and `area()` (to use body you must have area and pos)
        * The sprite didnt get affect by gravity (fall down)
    * Question: Am I missing something? Why isnt my sprite falling down even though I have all the requirment?
    * Next step: Ask Slack about why isnt my sprite falling down

* Kept trying to get `body()` to work by using `getGravity()`/`setGravity()`.
    * Didnt work

## 1/7/24

* Tried Learning `addlevel()`
	* Was trying to create a level but for some reason I cannot define the symbol as my sprite without an error. I tried using the example code and revising what symbols I'm missing but it always gives me a cannot define error.
	* Tried fixing my "" but most of the thing it "gave me a Level symbol def must be a function returning a componment list." error.
	* Question: Why is my code loading this error??
	* Tried for 45 minutes and I still cannot figure it out so I'm going to ask Mr.Mueller or slack

* Learned `anchor()`
	* anchor allows you to stay at one spot while rotating.
 	* I made my sprite `anchor(center)` and gave it different `rotate()` numbers like 7100, 200, 100. The sprite did not move spots while rotating. 
  
* Tried learning `DoubleJump()` by adding it into my code but realized I need a onground code to make it work

* Tried making my sprite fall due to gravity using `body()`
 	* DID NOT WORK. For some reason even though I added `area()`, and `pos()` my sprite just wont fall
    	* AFTER 30 minutes I FINALLY GOT MY SPRITE TO SLOWLY FALL DOWN.
     * I used `setGravity()` and `getGravity()` while using `body()` and my sprite was falling at the rate I set my gravity too
     * I removed `body()`, `area()` and `pos()`, and gravity stopped working, which means you NEED ALL OF THESE COMPONMENTS.
     * I played with how fast my sprite fall by changing the gravity. 500 made my sprite fall very quick but 1000 made it even quicker
 
* Tried learning `onClick()` but my RemoveAll was undefined.
	* `onClick()` only works outside an `add([])`

* Learned how to use `move(direction, speed)`
	* Made my bean sprite move RIGHT by 400 speed
	* Question: Can I make it move diagonal?
 		* Tinkering made me realize that if you want to move diagonal you can make it move and set a gravity so it goes right while going down
   

 
  







