### The Go Challenge 6

#### Daedalus & Icarus

**Preamble**

In Greek mythology, Daedalus was a skillful craftsman and artist. He is
the father of Icarus, and the creator of the Labyrinth. This Go
challenge will be unlike any previous one. You will be creating two bots
which will compete head to head with all of the other participants.

**Bot 1. Daedalus**

![labyrinth](https://raw.github.com/golangchallenge/gc6/master/resources/labyrinth.jpg)

Daedalus's job is to create a challenging Labyrinth for his opponent
(shadow Icarus) to solve. The Labyrinth must be 15 cells by 10 cells.
Icarus will be place in a random location which will be accessible to
the goal which is a set of wings. The Labyrinth must be fully enclosed
and there must be a possible solution. Icarus must be located in a
random location accessible to the treasure. The treasure (wings) must
also be in a random location that is accessible to Icarus.

**Bot 2. Icarus**

![icarus](https://raw.github.com/golangchallenge/gc6/master/resources/icarus-and-daedalus.jpg)

Icarus wakes up to find himself inside of a dark Labyrinth.  Due to
the darkness of the Labyrinth he can only see his immediate room and
if there is a wall or not to the top, right, bottom and left. He takes
one step and then can discover if his new cell has walls on each of
the four sides.

**Goals of the challenge**

Your goal is to write a maze generator and a maze solver to go head to head against other bots.

The goal is to have your Icarus solve your opponents Labyrinth the
fastest (lowest number of steps). Victory will require a cleverly
crafted maze as well as a intelligent solver.

We will run a big tournament to determine who has created the best
pair of Bots. Each round will consist of two entrants going head to
head.

We will run 500 simulations between opponents and take the average number of steps taken to solve the labyrinth. The competitor with the lower average steps will win and go onto the next round.  

Ground Rules:
  * Every maze generated must be solvable.
  * Both Icarus and the treasure must be randomly placed.
  * Mazes must be fully enclosed. The only way out is the treasure.
  * Mazes may have more than one correct solution.
  * No cheating. Don't miscount steps or anything like that.

This is meant to be fun. The hope for this challenge is to get you
thinking about how to write code in Go. We will be exposing you to
some of the basic libraries you would use to write both command line
applications and web services.

**Requirements of the challenge**

You will be given incomplete source code for application which you must complete. The structure and scaffolding of the application is there for you already done, but the critical logic is missing.

You will communicate with your opponent bot over a REST API. A
complete skeleton for the app structure will be provided to you to
ensure every bot has the same flags & endpoints.

This challenge makes use of 3 libraries outside the standard library:

* [gin](github.com/gin-gonic/gin) : One of the many web frameworks available for Go. I particularly like the speed and interface Gin provides.

* [cobra](github.com/spf13/cobra) : A Commander for modern Go CLI interactions. Used by Google’s Kubernetes, RedHat’s Project Atomic, Docker, OpenShift, CoreOS’s Rocket, Parse, GiantSwarm & GopherJS

* [viper](github.com/spf13/viper) : A complete configuration solution for Go applications. It is designed to work within an application, and can handle all types of configuration needs and formats.

There are 4 different operations already defined for the program.

* a bare `labyrinth` will run a server and connect your client to it to solve it
* `labyrinth daedalus` will run a server
* `labyrinth icarus` will run a client
* `labyrinth author` will output your given name
* `labyrinth help` will output help for these commands and the flags they take.

You will need to make changes to at least 3 files to complete your task.

You will need to:
* Put your name in the `var AuthorName = "spf13"` line in commands/labyrinth.go file
* Write the `createMaze()` function in the commands/daedalus.go file
* Write the `solveMaze()` function in the commands/icarus.go file

You may (and likely will want to) make other changes to these files but keep the integrity of the API intact.

Bonus features:

The default behavior of the `labyrinth` program is to run a server and connect to it with a client thus creating and solving a maze. This is really helpful for testing.

There is an additional library provided that will do nice things like providing a few interfaces and a `printMaze(Maze)` function that will print the maze to the terminal in ascii.

**Hints**

[This site](http://www.astrolog.org/labyrnth/algrithm.htm) is a pretty
good resource explaining different types of Mazes.

[Mazes for Programmers](http://www.amazon.com/Mazes-Programmers-Twisty-Little-Passages-ebook/dp/B013HA1UY4/ref=mt_kindle?_encoding=UTF8&me=) is also a helpful book.

**Special note for the evaluators**

Running `labyrinth daedalus` from competitor A and `labyrinth icarus --times 500` from competitor B is all that is needed for running a simulation.

**About the author: Steve Francia**

Steve Francia is responsible for two of the largest projects in Go
(and open source); He’s the Chief Operator of the [Docker
project](http://docker.com/) and the creator of
[Hugo](http://gohugo.io/), the most contributed-to community project
in Go. He loves open source and is thrilled to be able to work on it
full time, and then some. He has also created some of the most
widely-used Go libraries, including
[cobra](http://github.com/spf13/cobra),
[viper](http://github.com/spf13/viper) &
[nitro](http://github.com/spf13/nitro). In writing, Steve tweets as
[@spf13](http://twitter.com/spf13), blogs at
[spf13.com](http://spf13.com/) and has written a few books for
O’Reilly. In person, he enjoys giving talks & workshops and spending
time with the Go community around the world. When not coding, he is
usually having fun outdoors with his wife and four children.

**Steve has this to say about the challenge**

I thought it would be fun to play with Mazes. I don't really have any prior experiences with programming mazes and I learned a lot through this exercise. I hope you will enjoy it as well.
