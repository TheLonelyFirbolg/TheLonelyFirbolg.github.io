+++
title = "Factions and Goals"
date = "2024-06-28"
+++
A simple-ish mechanic for advancing faction goals, sparked by Dimension 20's new season *Never Stop Blowing Up* and inspired by Mausritter and a read through I saw of 24XX.
<!-- more -->
* For each goal a faction has, assign a target number (normally between 4 and 10) representing its difficulty.
* For each resource a faction has, assign a resource die.
* On each faction turn, a faction chooses one goal to advance using a relevant resource. Roll the resource die against the target number.

Check for the following in turn:
* On a roll equal to or above the target number, the faction achieves their goal.
* On a roll below the target number, mark a tally by the goal. On subsequenent rolls, a single tally point can be spent to increase the result by 1.
* On a result of the max number on the resource die, the resource die permanently increases in size by one step. This represents some improvement to the resource through the faction's ongoing efforts.

The actions of players could have a range of impacts, from increasing/decreasing a faction's resource die to affecting the target number of different goals. Player agency should obviously be prioritised, so be generous when ruling on their impact on faction play under this system.

## Example
The *Eagle's Claw* are a small gang operating between the under- and over- cities. They have the following resources:
* Small but loyal crew (d4)
* Ties to the *Goblin Girlies* (d4)
* Dirt on undercity officials (d6)

Their goals are:
* Start a protection racket near their undercity headquarters (TN 4)
* Kidnap the pet cat of a rival gang leader (TN 5)
* Establish a permanent base in the overcity (TN 8)

The most pressing issue is probably getting more revenue, so they'll leverage their dirt to get a blind eye turned on racketeering efforts. On their first faction turn, I roll a 3, marking one tally by the goal. Maybe this official doesn't have much authority in this particular area. On their next turn they try again, rolling a 6, increasing their dirt to a d8 resource and succeeding on the goal. So perhaps they sought out dirt on some other administrators and found something big, establishing their racket and getting this official completely in their pocket. We could then add a new goal.

On turn 3, they try and outsource the catnapping to the *Goblin Girlies*, who fail with a 1. They try again on turn 4 with their own crew, getting a 3 which can be pushed up to a 4 by spending the tally from their previous attempt. This increases the die of the crew to a d6. It then took me 5 rolls to hit a 4+, but they do eventually get the cat.

## Thoughts and guidance
This is completely untested. I run some numbers below to simulate what results it would lead to for different target number and resource die sizes. It seems quite simple and easy to track and set up. I'll be trying it out in my long-running 5e campaign, where I've recently felt the lack of a system for advancing NPC/faction goals, so I might write a follow up with some more thoughts after testing.

If a faction has 2 relevant resources, maybe roll both dice and then choose one to use for the resolution. This means only one resource can improve on a faction turn, but there's still an advantage to having multiple relevant resources.

I would probably stop marking tallys at 4, as they're only useful to increase a die's size or reach the TN and therefore won't be used much.

## Maths
First, lets look at what happens without the tally points on a fail.
On average, [it takes a dX X rolls to roll X](https://math.stackexchange.com/questions/1119872/on-average-how-many-times-must-i-roll-a-dice-until-i-get-a-6). So 4 turns for a d4 to roll 4 and 12 turns for a d12 to roll 12. So for a target number of 5 and a d4 resource die, we expect the die to increase to a d6 on turn 4. Then we need to roll a 5 or a 6, and we find this is expected to take 3 turns using a similar formula. So in total 7 faction turns.

**Number of turns to reach different TN for different starting dice**

| Starting Faction Die | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| d4 | 4 | 7 | 10 | 14 | 18 | 23 | 28 |
| d6 | 2 | 3 | 6 | 10 | 14 | 19 | 24 |
| d8 | 1.6 | 2 | 2.7 | 4 | 8 | 13 | 18 |
| d10 | 1.4 | 1.7 | 2 | 2.5 | 3.3 | 5 | 10 |

These are really quite long, to the point that it cuts out smaller resource dice from being feasible. So lets try this again using the tally points on a fail rule. The maths gets a bit more tricky here. This is my estimate of what we now get.

**Number of turns to reach different TN for different starting dice**

| Starting Faction Die | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| d4 | 2 | 4 | 5 | 7.7 | 9 | 11.3 | 15 |
| d6 | 1.5 | 2 | 3 | 5.7 | 7 | 9.3 | 13 |
| d8 | 1.3 | 1.6 | 2 | 2.7 | 4 | 7.3 | 9 |
| d10 | 1.3 | 1.4 | 1.7 | 2 | 2.5 | 3.3 | 5 |

It's now still gonna take a while for a faction with poor resources to achieve harder goals, but not prohibitively so. And through the course of this, their resources improve and subsequent goals will be more easily achieved. For a longer sandbox, I could see this feeling quite organic, as smaller factions take a while to become major players. It's also worth noting that if the same resource can be used for different goals, all of these goals will become easier as the resource die increases. This is another element which feels quite intuitive to the world.
