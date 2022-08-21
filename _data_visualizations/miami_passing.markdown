---
title: Miami Heat Passing Sequences
layout: projects
---
I created this visualization with the idea to analyze passing sequences. This has just been done for a single game, but the hope is to create this for an entire season's worth of data. However, an automated way of obtaining this data is needed, as this was recorded manually. 

**Hypothesis**: Longer passing sequences result in successful possessions more often than shorter sequences. 

This visualization represents all passing sequences initialized by Jimmy Butler of the Miami Heat against the LA Lakers in game 5 of the 2020 NBA Finals. The player who initializes the possession is the player who brings the ball past half court or inbounds the ball in the frontcourt. Only possessions initialized by Jimmy Butler are shown here. Jimmy Butler accounted for 73.3% of all initializations. Summary statistics by passing layer are shown. For example, FGA for the 1st pass layer represents the number of Field Goals Attempted for all players who received the first pass in a passing sequence. All data recorded **manually** from game 5 of 2020 NBA Finals and can be found [here](https://github.com/brendenconnors/HW4-Network).

Hover over specific nodes to see outcomes!

{% include Sankey_custom_data.html %}

