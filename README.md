# Classifying MLB Pitch Zones and Predicting MiLB Zone

## Statcast Pitch Classification

### Zones

Within the MLB Stats API and Baseball Savant API, pitch locations are classified into 12 zones, as illustrated in Figure 1. These zones, as seen from the catcher’s perspective, define the strikezone and relative locations of a pitch. For example, a pitch inside “Zone 1” would be classified as a “Strike” and “up and away” to a left handed batter. In the same vein, a pitch located in zone 11, 12, 13, or 14 (and beyond) is outside of the strikezone, and would be classified as as “Ball”

### Zone Metrics

The zone classification of pitches allow analysts to calculate plate discipline metrics beyond the conventional metrics such as Whiff% and Swing%. An example of a metric that can be calculated using these zone classifications is Out-of-zone Swing Rate, also known as Chase% or O-Swing%. O-Swing% calculates the rate at which a batter swings at pitches that are “Out-of-zone”, and is a large driver in a batter’s plate discipline outcomes. Intuitively, batters which swing at fewer pitches outside the zone tend to have higher walk rates (BB%). The more “Balls” a batter takes, the more likely they will walk.

Another example of a zone plate discipline metric is In-Zone Swing Rate (Z-Swing%). Similar to O-Swing%, Z-Swing% calculates the number of pitches “In-Zone” which a batter swings. In terms of contact, batters perform significantly better against pitches that are thrown inside the strikezone than ones that are not. The following table summarizes the Estimated wOBA on Contact (xwOBACON) for pitches inside and outside of the strikezone during the 2023 MLB Season.


Table 1: 2023 MLB xwOBACON In-Zone and Out-of-Zone
| In Zone   |   xwOBACON |
|:----------|-----------:|
| False     |   0.284 |
| True      |   0.393 |

Batters which consistently swing at pitches inside the strikezone are more likely to perform at a higher level than those that do not. Figure 2 illustrates the xwOBACON of each of the zones during the 2023 MLB Season. Pitches thrown near the heart of the plate tend to be more favourable for batters compared to those further away from the centre.
