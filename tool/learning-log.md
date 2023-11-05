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
