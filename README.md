# MLB-Pitch-Classification-Model-R
Using machine learning modeling to classify major league pitch types using real play-by-play data

## Rationale

Major League Baseball (MLB) stadiums are equipped with a 12 camera system that captures data for every pitch thrown in a game. If you've ever watched a major league game, you'll know what the pitch is identified almost instantly by this system both on TV broadcasts and inside the stadium. 

### But, how do their systems know which pitch was thrown, and which metrics are most influential in allowing these systems to identify a pitch? 

The aim of this project was to create a machine learning model that can classify MLB pitches using real MLB play-by-play data scraped from baseballsavant.mlb.com, to understand which metrics are the most important when identifying/classifying a pitch in the major leagues. 

## Data Definitions

### Data for this project were scraped from baseballsavant.mlb.com and include over 19,000 pitches from the last 5 days of major league play since the 2024 all-star break. 

pitch_name = The name of the pitch derived from the Statcast Data.

release_speed = Pitch velocities from 2008-16 are via Pitch F/X, and adjusted to roughly out-of-hand release point.

release_pos_x = Horizontal Release Position of the ball measured in feet from the catcher's perspective.

release_pos_z = Vertical Release Position of the ball measured in feet from the catcher's perspective.

pfx_x = Horizontal movement in feet from the catcher's perspective.

pfx_z = Vertical movement in feet from the catcher's perpsective.

plate_x = Horizontal position of the ball when it crosses home plate from the catcher's perspective.

plate_z = Vertical position of the ball when it crosses home plate from the catcher's perspective.

release_spin_rate = Spin rate of pitch tracked by Statcast.

release_extension = Release extension of pitch in feet as tracked by Statcast.

spin_axis = The Spin Axis in the 2D X-Z plane in degrees from 0 to 360, such that 180 represents a pure backspin fastball and 0 degrees represents a pure topspin (12-6) curveball

## Key Findings

Our model could identify MLB pitches with just under 92% accuracy. These innacuracies typically came when attempting to classify the lesser used pitches. 

### Of all metrics gathered by the MLB and statcast, the following appear to be the most important when aiming to classify a pitch type:

- Vertical movement in feet from the catcher's perspective.
- Pitch velocity
- Horizontal movement in feet from the catcher's perspective.

This speaks volumes to just how much pitchers are able to manipulate their pitches, given that the movement on the ball between the mound and the plate are two of the top three metrics. Of course, we all know that velocity plays a large role in pitching, but here it also plays a big role in identifying a pitch also. Overall, this model performed well, correctly classifying 92% of pitches, and even better when identifying the more common pitch types such as four seam fastballs and splitters.
