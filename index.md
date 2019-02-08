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
This reasoning behind this project was pretty simple. I wanted to be able to generate pixelated curves easily but I could not find any online so I created my own. This program uses TkInter and python. The user puts in a bunch of points and the program creates a spline. That's all there is to it.

![Capture](https://user-images.githubusercontent.com/20815153/51453570-461a3a00-1d94-11e9-88dc-eb1c8e3289d2.png)

&nbsp;

&nbsp;
* * *
# Programming with OLC (C++)
"OLC" a.k.a `Javidx9` is the creator of a small opensource engine written in C++ called olcPixelGameEngine. I have been following along with his development of the engine and creating some projects of my own with it.

## olcEyes
This is a proof of concept main menu of a video game where the eyes follow the cursor around the screen and shimmer. 

![olceyesgif](https://user-images.githubusercontent.com/20815153/52453869-6708ca80-2b9d-11e9-8b94-284efb7997c0.gif)


&nbsp;

&nbsp;
* * *
## olcDungeon



&nbsp;

&nbsp;
* * *
## olcGuiDemo



&nbsp;

&nbsp;
* * *
## Nonogram Solver



&nbsp;

&nbsp;
* * *
## Tetris



&nbsp;

&nbsp;
* * *
# More C++ projects
## Sudoku Solver



&nbsp;

&nbsp;
* * *
## MC Item Tree



&nbsp;

&nbsp;
* * *
## PNN Bot

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
