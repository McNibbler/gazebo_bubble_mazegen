# Gazebo Bubble Mazegen
**Thomas Kaunzinger**
*CS4610*

This python based maze generator uses XML to generate simple random "bubble mazes."

These worlds consist of a number of randomized square walls throughout, with no outer
perimeter. While this map is quite simple on its own, it's intentionally designed
to be as non-wall-crawl-friendly as possible.

As there is no perimeter, it is trivially easy for a wall-follow robot to get stuck
by going the entirely wrong direction into space.

Similarly, if the wall-follower *does* find a wall, since they are all square "bubbles,"
the robot is guaranteed to be stuck in a cycle, as each bubble is its own island.

The only way to find the end is to have some methodical means of knowing the end's
direction and creating a path to get there, such as through an Astar pathing algorithm.
