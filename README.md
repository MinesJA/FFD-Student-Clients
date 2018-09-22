Flatiron Field Day
===============
A forked version of the repo deployed to students at Flatiron's Field Day event. The purpose of the event was to have students compete to programmatically protect the color of their section of a Canvas board from being overwritten and to attempt to overwrite the color of competeing teams. Flatiron Staff built the clients in this repo to allow allow students to write to and read from the board in Javascript, Ruby, or Python (whichever language they were more comfortable in). Staff also built a intermediary Node backend, hidden as an NPM package, which intercepted calls to the board, queued them, and processed them at a specific rate. Those POST requests were then sent to the real server which allowed writing to the board.

![Field Day Timelapse](https://j.gifs.com/D93Rx6.gif)
Format: ![Alt Text](https://j.gifs.com/D93Rx6.gif)

## Getting Started
* See instructions deployed with repo on the day of the event below
* [Canvas Board Client](https://github.com/MinesJA/spotify_tree_backend)
* [Backend Repo](https://github.com/MinesJA/spotify_tree_backend)

## Built With
* [Node.js](https://nodejs.org/en/)
* [Ruby](https://www.ruby-lang.org/en/)
* [Express](https://expressjs.com/)
* [Python3](https://www.python.org/download/releases/3.0/)
* [NPM](https://www.npmjs.com/)

## Authors
* [Jonathan Mines](https://github.com/MinesJA)
* [Steven Balasta](https://github.com/sbal13)
* [Daniel Seehausen](https://github.com/DanielSeehausen)

## License
This project is licensed under the MIT License


Client Instructions
===============

# Flatiron Field Day 

Hello and welcome to Flatiron Field Day! Today, you and your team will have the opportunity to create a mosaic using your programming skills. 

Right now, we are hosting a server that stores a board full of tiles, and it is the job of your team to write scripts that will allow you to set the color of individual tiles, thus painting your masterpieces for all the world to see.

To aid you in your programmatic art endeavors, we have written some clients to help you.


### The Nexus

Everyone, regardless of language, should be running the Nexus. To do this, please `cd` into the directory called `nexus` and run 

```
npm install
``` 

in your terminal. When that's done, run

```
npm config set nexus:teamID <INSERT YOUR TEAM ID>

ex: npm config set nexus:teamID 1
```
**Note** You should have been given a team ID. If you do not know yours, please ask!

Finally, run

```
npm start
```

And that's it! If all is well, you should see 

```
Example app listening on port 3001!
CONNECTED
```

in your terminal. Leave this terminal window running in a background. Easy!

### User Clients

So that everyone can participate regardless of language preference, we've written clients in Ruby, JavaScript, and Python.

The basic gist of each client is the same. 

At your disposal are four methods:

1. Get Tile
	Given an x and y coordinate from the board, this function will return to you data about the Hexidecimal color stored at that location.
2. Set Tile
	Given an x, y, and valid Hexidecimal color, this function will write that color to the pixel specified by your coordinates. Your requests will be automatically queued and sent to the server.
3. Get Queue
	This function will return to you your queued requests.
4. Clear Queue
	This function will clear your queue, effectively allowing you to cancel any unsent Set Tile requests you may have made.
