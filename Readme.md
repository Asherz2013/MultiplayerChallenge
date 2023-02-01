# Mutiplayer test

This project is to test out my multiplayer skills.
The idea was to have 2 players work together to exit a room.

Think Escape room vibes.

## What did I learn

Networking is hard.

However, Unreal does a very good job to do most of the heavy lifting.
Creating a third person template, means that the the Character Pawn is ready to replicate out the box.

The Character Movement component does all the heavy lifting, allowing the players to move, rotate and jump around the level.

### Creating new actors

I created a new object, which I would use as a Pickup item, to get this to replicate, I needed to tick the "Replicate" option and it pretty much worked as expected.

I made sure that when I did any form of collision detection that it was ran on the Server side with `has_authority`.

### Adding a new variable

I also added a new variable to the Player Character, which was to hold their personal score. I again made sure this was replicating so that I could display it on all players HUD.

However, once I got a HUD working on the players, it seemed as though the replication was not being triggered correcty. As the HUD on the Client, would only update once they collected a coin. Which was not the behaviour I was after.

I spent the afternoon trying to figure out why but sadly at this time of writing this I did not come to a conclusion. I will update this section once I figure out why.

## Stretch Goals

I had some stretch goals of this project which I will list below:

- Add a Lobby, so that players could join their friends when ever
- Be able to transition to a new level
- Add some more mechanics that collecting coins.
