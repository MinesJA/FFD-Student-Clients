# Flatiron Field Day 

Hello and welcome to Flatiron Field Day! Today, you and your team will have the opportunity to create a mosaic using your programming skills. 

Right now, we are hosting a server that stores a board full of tiles, and it is the job of your team to write scripts that will allow you to set the color of individual tiles, thus painting your masterpieces for all the world to see.

To aid you in your programmatic art endeavors, we have written some clients to help you.

[Visit rest of the code base](https://github.com/MinesJA/fi-field-day)

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




