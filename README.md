### The Go Challenge 6

#### Challenge title

**Preamble**

In Greek mythology, Daedalus was a skillful craftsman and artist. He is
the father of Icarus, and the creator of the Labyrinth. This Go
challenge will be unlike any previous one. You will be creating two bots
which will compete head to head with all of the other participants.

**Bot 1. Daedalus**

Daedalus's job is to create a challenging Labyrinth for his opponent (shadow
Icarus) to solve. The Labyrinth must be 20 cells by 20 cells. Shadow
Icarus will be place in a random location which will be accessible to
the goal which is a set of wings. The Labyrinth must be full enclosed
and there must be a possible solution. Icarus must be located in a
random location accessible to the solution.

**Bot 2. Icarus**

Icarus wakes up to find himself in the middle of a Labyrinth. Due to the
darkness of the Labyrinth he can only see his immediate cell and if
there is a wall or not to the top, right, bottom and left. He takes one
step and then can discover if his new cell has walls on each of the four
sides.


**Goals of the challenge**

Your goal is to write these pair of bots to go head to head against
other bots. The goal is to have your Icarus solve your opponents
Labyrinth the fastest (lowest number of steps).

We will run a big tournament to determine who has created the best pair
of Bots. Each round will consist of two entrants going head to head. We
will run at least 50 different games to determine winner. In the event
of a tie we will run more simulations. The winner will go onto the next
round.

You will communicate with your opponent bot over a REST API. A small
skeleton for the app structure will be provided to you to ensure every
bot has the same flags & endpoints.

This is meant to be fun. The hope for this challenge is to get you
thinking about how to write code in Go. We will be exposing you to some
of the basic libraries you would use to write both command line
applications and web services. Think of this as a microservice
introduction with an element of competition.

**Requirements of the challenge**

Bonus features:

**Hints**

[This site](http://www.astrolog.org/labyrnth/algrithm.htm) is a pretty
good resource explaining different types of Mazes.

**Special note for the evaluators**

**About the author: Steve Francia**

Steve Francia is responsible for two of the largest projects in Go (and
open source); He’s the Chief Operator of the [Docker
project](http://docker.com/) and the creator of
[Hugo](http://gohugo.io/), the most contributed-to community project in
Go. He loves open source and is thrilled to be able to work on it full
time, and then some. He has also created some of the most widely-used Go
libraries, including [cobra](http://github.com/spf13/cobra),
[viper](http://github.com/spf13/viper) &
[nitro](http://github.com/spf13/nitro). In writing, Steve tweets as
[@spf13](http://twitter.com/spf13), blogs at
[spf13.com](http://spf13.com/) and has written a few books for O’Reilly.
In person, he enjoys giving talks & workshops and spending time with the
Go community around the world. When not coding, he is usually having fun
outdoors with his wife and four children.

**Steve has this to say about the challenge**


