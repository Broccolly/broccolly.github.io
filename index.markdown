---
layout: default
---
# Portfolio Highlights
Here's some personal highlights from both my professional and hobbyist life!

## Physics Programming on Snake Party (C++, in-house engine, Sumo Digital)
Following 11 straight years studying maths and physics I finally decided to try something different and began working towards a Level 7 Apprenticeship at Sumo Digital in Sheffield. This has allowed me to work on several projects I am proud of, but perhaps my favourite is the physics engine I developed for the [Snake Party](https://www.sumo-digital.com/sumo-digital-academy-create-a-halftime-hit-for-sheffield-wednesday-football-club/) project we worked on in collaboration with Sheffield Wednesday Football Club.

<iframe width="560" height="315" src="https://www.youtube.com/embed/EqPuux4oIP8?si=p7VVAR5LNU8MoRXW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Our team recreated the look and feel of the Sumo Digital hit game Snake Pass (2017) to make a local multiplayer game for football audience members to play at half-time. We needed a robust physics system which could handle wiggling snake bodies, collisions between them and the environment and allow for snakes to grow and shrink dynamically as the game progressed.

I dove into the world of real-time physics, finding the writings of [Erin Catto](https://box2d.org) especially helpful, and got to work implementing a physics engine. I wrote the physics system from scratch in C++ as a static library that could be in other projects. I used a fully constraint-based approach to resolve collisions, friction and restitution, and implemented broad and narrow phase collision detection algorithms for spheres, AABBs, and OBBs.

## Junior Programming on Nutmeg! (C++, Sumo Digital)
My most recent project as a junior programmer has been on 'Nutmeg!' a 1980s inspired football management card game for PC coming in 2026. I can't share too much about my role specifically just yet unfortunately, but it's been fantastic working on a game that will be released to the public and seeing the full game development cycle from beginning to end.

<iframe width="560" height="315" src="https://www.youtube.com/embed/oWrVxXGlg6w?si=i2opHJQvkA0ExunX" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


## Ludum Dare 53 - Pack it In! (Unity / C#)
During my studies at university I became interested in making games as a hobby and took part in several game jams to hone my skills. I learnt Unity and C# using online tutorials, and by my third game jam, Ludum Dare 53, I felt comfortable with the engine and was able to make a full game in a weekend. I made this game 'Pack it in!' on the theme of 'Delivery', with my friend Sam, who made the audio for the game.

The game involves sorting different coloured parcels into their respective delivery vans by clicking on the sorting arms to control the direction they get sorted in. Give it a go below!

The game was my most successful jam game at the time, landing us in the top 20% of submissions in the 'Overall' category, and the top 10% of submissions in the 'Innovation' category. More details can be found on the game's [itch](https://broccolly.itch.io/pack-it-in) page.
<iframe frameborder="0" src="https://itch.io/embed-upload/7827308?color=333333" allowfullscreen="" width="720" height="540"><a href="https://broccolly.itch.io/pack-it-in">Play Pack It In! on itch.io</a></iframe>
(Note that the full screen option, and Windows OS Custom Scaling causes issues with UI and map scaling - try setting Windows scale to 100%. A Windows build can be found [here](https://broccolly.itch.io/pack-it-in) which doesn't have these issues!)


## Ludum Dare 55 - Lift Summoner Deluxe 1997 (Pico-8 / Lua)
Following several game jams using Unity/C# and using C++ at work, a friend ([ehmtang](https://github.com/ehmtang)) and I wanted to use a framework with more limitations to help us approach game dev differently. We settled on using [Pico-8](https://www.lexaloffle.com/pico-8.php), a fantasy console which emulates an old-school games console with a 128x128 pixel screen size, a 32kB game size, and a fixed 16 colour palette.

Pico-8 uses Lua as a scripting language, which we learnt in preparation for the jam, and found the simplicity of it challenging after using the significantly more flexible C++ and C#. In particular, Lua does not directly have a concept of classes, but they can be emulated using Lua's metatables. We created a basic framework to allow us to create game objects and flow states before the jam started, to help us manage these complications.

The game we made was Lift Summoner Deluxe 1997: Kitten Edition. In the game, you play as an elevator manager in a busy office building helping visitors get to their floor before they become angry. I was responsible for implementing the behaviour of the visitors, the mechanics of the lifts, and the scoring system, as well as other bits and bobs. The music was made by [jemh2k](https://soundcloud.com/jemh_music). This game reached the top 10% of submissions in the 'Overall' category for the jam.

<iframe frameborder="0" src="https://itch.io/embed-upload/10192651?color=333333" allowfullscreen="" width="720" height="540"><a href="https://broccolly.itch.io/lift-summoner-1997">Play Lift Summoner Deluxe 1997: Kitten Edition on itch.io</a></iframe>
To play the game, use the 'x' key to start, and then the arrow keys and 'x' to select a level. Once playing, use the arrow keys to select a lift, x to open its doors, and up and down to move it up and down. The lift doors will close automatically after letting people out, to stop anyone getting in the wrong lift by mistake! You can find more details on [itch](https://broccolly.itch.io/lift-summoner-1997).

## Ludum Dare 58 - Deep Flied Donut (Godot/GDScript)
Further wanting to explore different engines and styles of programming, I decided to use Godot in my most recent jam to make '[Deep Flied Donut](https://broccolly.itch.io/deep-flied-donut)' with my brother. You can give it a play at the link above.

It was interesting using Godot for this project as it imposes a different design philosophy than other engines with its nodes and signals structure. This took some time to get my head around, particularly with regards to how to compose scenes and how to avoid strong coupling between nodes by using dependency injection.

To implement the physics in the game, I used a signed distance function (SDF) for the combination of the donut and the web, which gave the force and direction of the force that should act on the spider at any position. I used this approach as some of the built in collider functionality in Godot does not work with concave collider shapes, which would include the toroidal collider of the donut.