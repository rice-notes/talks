# New Frontiers in Imitation Learning

Yisong Yue - Associate Professor, Caltech

## Motivations

Behavioral Modeling - We're in an era where we're tracking nearly all
behavioral data.  

* Tracking technologies are deployed in nearly every NBA and
  Soccer stadium to track player movements
* There's also tracking of the agents and cameramen
* Disney tracks facial expressions and emotions during movie screenings
* Taxi Data

Lots of data 


## Imitation Learning

Generalization of supervised learning, the input is a sequence of actions, and 
the output is a sequence of actions.  

Example: Basketball Player Trajectories

Input: Player position data, $$a$$
Output Next move of a player, $$s$$

### Previous Work

Work has ranged from value function learning to policy based learning, as well
as online and offline learning.  However, past work has mostly been spent on 
deep imitation learning that doesn't assume structure of the data, and builds 
very complex models.  

### Speech Animation

* Animation artists spend most of their time designing mouth and eyes
* Not much room for creativity, as you have to keep a character's face consistent
* Can we automate?
