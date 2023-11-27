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











