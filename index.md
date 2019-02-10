---
layout: default
---
# Projects in python
## [Discord Bot](https://github.com/twalford/discordbot)
The bot started off as a pokedex (a list of all pokemon) for a discord server of three people. You would give the bot a number range and it would give you back the pokemon IDs within that range.

![dexr](https://user-images.githubusercontent.com/20815153/52334640-4a14b000-2a54-11e9-888c-d5138874d791.PNG)

It was a simple idea and it worked well enough for us. We quickly grew bored of the pokemon and I started adding commands that would send back gifs and images and text/emojis for our inside jokes. One way to describe it would be a filing cabinet of memes. I added a scoring/currency system `Ponks` which we could trade with one another and we could see how many we saved up with the leaderboard.

![lb](https://user-images.githubusercontent.com/20815153/52334646-4d0fa080-2a54-11e9-98da-f3220ba58940.PNG)

Every gif-producing command would cost a certain amount of `Ponks` and the bot would receive them in a transaction. We needed a way to get the currency back so I added a Pinata event that would trigger once the bot had reach a certain amount. It required all members to use the `.smack` command, dropping a random percentage of `Ponks` on the ground with every wave of smacks.

Other features of the bot include:
- Note system:
  - Add a note to the system.
  - Ask the bot to pick a random note.
  - Purge (snap) half the notes.
- Oxford Dictionary API:
  - Ask the bot to define a word.
- Minecraft Server Status API
  - Show all online players on a certain server.
- Maps of the world:
  - Ask the bot to show a map of a country or region.
- Random Emoji:
  - Ask the bot to pick up to 10 random emojis.
- Flip a coin.
- Roll a dice.
- Guess a number between 1 and 100 for the chance to win `Ponks`.
- Slap each other to make them drop some `Ponks`.
- Insert your own character into a copypasta.
- Various gifs and video links.

&nbsp;

&nbsp;
* * *
## [Schem Slicer](https://github.com/twalford/schem-slicer)
Schem Slicer is a program that slices up `.schematic` files and turns them into images. A `.schematic` file is created by third-party programs that can store sections of a Minecraft world. The purpose of Schem Slicer was to provide a much more manageable way to copy and reference parts of a schematic.

![slicer](https://user-images.githubusercontent.com/20815153/52335924-b80ea680-2a57-11e9-988c-6e9dbdfe776c.PNG)

This was the first time I experimented with command line arguments in a program and I ended up adding a few options for the user to use:
- Choose the axis to slice along.
- Automatically crop the image.
- Flip the image.
- Generate the images with its index in the corner.
- Include a grid on each image.
- Change the background colour on the images.

When the program has finished running, the user will be left with a folder full of images depicting the slices of the schematic.

![out](https://user-images.githubusercontent.com/20815153/52335919-b644e300-2a57-11e9-89a3-392593f6ccb6.PNG)

Here is a look at one of the images in its entirety. In this example I used a schematic that when created in-game turns into pixel art (a 128x128 portrait of a friend).

![1](https://user-images.githubusercontent.com/20815153/52335928-ba710080-2a57-11e9-9c5b-ed018538e748.png)

&nbsp;

&nbsp;
* * *
## [Pixel Spline](https://github.com/twalford/pixel-splines)
The reasoning behind this project was pretty simple. I wanted to be able to generate pixelated curves easily but I could not find any online so I created my own. This program uses TkInter and python. The user puts in a bunch of points and the program creates a spline. That's all there is to it.

![Capture](https://user-images.githubusercontent.com/20815153/51453570-461a3a00-1d94-11e9-88dc-eb1c8e3289d2.png)

&nbsp;

&nbsp;
* * *
# Programming with OLC (C++)
"OLC" a.k.a `Javidx9` is the creator of a small opensource engine written in C++ called olcPixelGameEngine. I have been following along with his development of the engine and creating some projects of my own with it.

## [olcEyes](https://github.com/twalford/olcEyes)
This is a proof of concept main menu of a video game where the eyes follow the cursor around the screen and shimmer. 

![olceyesgif](https://user-images.githubusercontent.com/20815153/52453869-6708ca80-2b9d-11e9-8b94-284efb7997c0.gif)

The eye is split into three parts:
- The eye socket
- The iris
- The pupil

The socket stays still while the iris and pupil move in relation to the cursor. The iris and pupil are seperated because I wanted them to move at slightly different amounts to give a sublte 3D effect. All three parts are represented as a 2D array of floats. The shimmering effect comes from a sine function of the elapsed time of the program combined with a randon number generator that sets the size of each square on every frame.

&nbsp;

&nbsp;
* * *
## [olcDungeon](https://github.com/twalford/olc-dungeon)
olcDungeon was my attempt to clone `Redungeon` - an endless action platformer game published by nitrome. The aim of the game is to progress forward as far as you can without falling off the platforms and into the darkness below. The game generates a path of `dungeon modules` for the player to navigate: some containing walls to walk around, ice to slide across, fire to avoid, and portals to teleport to. Below is an example of gameplay at its current state.

![dungeondemo](https://user-images.githubusercontent.com/20815153/52529907-5b5d0580-2d4f-11e9-8ea4-25a413ceb849.gif)

Much like any other video game in existence, I needed a testing level during development where I could test of all of the implemented features and tiles. On the left side of the level you can see the `WEAK GROUND` that starts to fall apart when the player stands on it. Directly next to that are the different coloured portals which are one-way teleports. In the middle there are pots of gold which crack and then break when the player runs into them. That is how the player collects coins (which serve no purpose in my clone). There is also a `WEB` tile which if the player steps onto, requires them to press a random sequence of keys to escape.

![dungeontestlevel](https://user-images.githubusercontent.com/20815153/52529905-5ac46f00-2d4f-11e9-925d-d08714fc44d2.gif)

This game was the most complicated project I had attempted so far (at the time) and it required me to also make a level editor. To make this level editor I repurposed a sprite editor also made by Javidx9 in the same engine. I transformed this sprite editor into a `DUNGEON MODULE` editor and created my own file type `.dumo` (short for Dungeon Module). The editor allows the user to load and save these `.dumo` files to disk with the F9 and F10 keys. The user can edit the modules by selecting a tile type and placing it in the module. Here is an example.

![dumoplacement](https://user-images.githubusercontent.com/20815153/52529908-5b5d0580-2d4f-11e9-80d5-a4fffbf0358d.gif)

The tiles are selected using number keys 1 to 9. There are more than 9 tiles, so I split them into tabs or "sets" which can be selected with keys F1 to F4 as seen below. Notice the 4 dots in the top left representing the tabs.

![dumotabs](https://user-images.githubusercontent.com/20815153/52529906-5b5d0580-2d4f-11e9-868b-2bd0cfee6644.gif)

I also had to implement a way to make the module larger or smaller by deleting and inserting rows/columns. To do this the user can press `C` to activate cropping mode, in which a line of red boxes will appear. The orientation is changed with `V` and the user can insert on the green side with the `Insert` key, and delete the highlighted row/column with, you guessed it, the `Delete` key.

![dumoinsert](https://user-images.githubusercontent.com/20815153/52529909-5bf59c00-2d4f-11e9-863e-bb417171c8fe.gif)

&nbsp;

&nbsp;
* * *
## [olcGuiDemo](https://github.com/twalford/olcGuiDemo)



&nbsp;

&nbsp;
* * *
## [Nonogram Solver](https://github.com/twalford/pgeHanjie)



&nbsp;

&nbsp;
* * *
## [Tetris]()



&nbsp;

&nbsp;
* * *
# More C++ projects
## [Sudoku Solver]()



&nbsp;

&nbsp;
* * *
## [MC Item Tree](https://github.com/twalford/mc-raw-items)



&nbsp;

&nbsp;
* * *
## [PNN Bot]()

***

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://assets-cdn.github.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
