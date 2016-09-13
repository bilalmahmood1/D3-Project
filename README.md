## Data Visualization
#### [Interesting Findings In The Baseball Data Set](https://bilalmahmood1.github.io/D3-Project/)

### Summary
Chart 1: Right handed batsmen are most common and there is association between batting performance and batting handedness;left handedness batsmen hit on average more home runs.

Chart 2: There seems to be players that have 0 batting average--there are quite a few blue dots. In addition, rarity of red dots for home runs suggests that hitting them is indeed really hard. Plus, not surprisingly,weight and height seems to have a linear relationship.

### Design

In chart one I had small set of summary numbers for different batting handedness and I wanted to compare among them. Thus the most likely choice was encoding aggregated numbers like number of players, mean home runs for each group etc., as length of a rectangle. And for the handedness categories (R,L and B), I chose position. Thus, I made an interactive  bar chart that could help compare aggregated summary for different batting handedness. In addition, I colored the handedness category with the highest summary number ,like R handed batsman were  most common in the data set thus leveraging reader’s pre-attentive processing abilities.


For the second chart I used the whole baseball data set and wanted to compare each player in terms of their batting average and home runs they have scored along with their their physical appearances i.e. considering their weight and height. In addition, I also wanted the readers to look at the plot and find quickly best and worst players in terms of their batting average and the number of home runs they have scored along with their physical dimensions as well. In order to achieve that, I used two axis, x and y for encoding weight and height of each player, encoded as circle’s position, and used diverging color scale to encode average/home runs for each player around the median value as circle’s fill.  Thus, in this way readers can find best/worst players quite quickly, once again leveraging on reader’s pre-attentive abilities. Moreover, I selected diverging color scale for filling each circle from colorbrewer2 and selected red and blue extremes considering color--blinded people. In addition, plotting around 1100 points raised the issue of overplotting, raised by one particular reader's feedback, and I avoided it partially by adding little bit of random noise to weight and height for each player.


### Feedback
```
Displaying only aggregated statistics about the baseball players. Like player numbers, their group average and group HR for three batting handedness.
```
*Added another chart that allows to compare among players in terms of their physical appearance and their individual home runs and batting averages.*
```
Scatterplot/bubble chart had points overlapping on top of each other and thus obscuring few players.
```
*Added little random jitter to each player's weight and height and thus reduced the overlapping problem. Didn't try varying opacity for each data point as it would be less effective in this case.*
```
Tooltip text was not displaying actual home runs and averages of the players.
```
*Modified tooltip text to show actual numbers (HR/avg) for each baseball player.Thus allowing readers to access actual values along with color encoding*

### Resources
- [Mike Bostock’s D3 scatterplot example](http://bl.ocks.org/mbostock/3887118)
- [Color for Bar chart](http://www.colorcombos.com/color-schemes/2511/ColorCombo2511.html)
- [Diverging color for scatterplot](http://colorbrewer2.org/#type=diverging&scheme=RdYlBu&n=7)
- [Scott Becker's D3 tutorials](http://synthesis.sbecker.net/articles/2012/07/08/learning-d3-part-1)
- [Make Effective Data Visualization](https://classroom.udacity.com/courses/ud507)

