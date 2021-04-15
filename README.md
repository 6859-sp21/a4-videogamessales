[Website Link](https://6859-sp21.github.io/a4-videogamessales/visualization.html)

# Rationale for design decisions

Our visualization uses a bar graph to show global sales of the top 15 video games in the current data subset and a treemap to show the percentages of regional sales that contribute to the global sales amount for each video game data point. When a user hovers over a bar, additional information about the particular video game, such as name, rank, platform, etc., pop up via a rectangular tooltip. 

For our primary visualization, we considered either using a bar graph or a circle/point graph. A circle/point graph would be ideal for a situation in which clustering patterns for both axes is important. However, the way we laid out our axes, the x-axis is only for ordering; there is no numerical significance. 

For our secondary visualization, we debated on whether we should use a treemap or a piechart. Both fulfilled the purpose we wished for our secondary visualization, which is to show the percentage of sales each region contributed towards the global sales of a particular video game, but given the popularity in visualizations overall, we decided on the treemap so general users will be looking at a visual encoding they are well accustomed to and can focus on what it is showing. 

To see the treemap, we debated on whether the user should hover or click on a bar representing a video game. We asked the audience in our video presentation what they preferred, and they said hovering seems to be the way to go because it is more intuitive than clicking on a bar. We as a team also agree on this; when considering that there are no lengthy descriptions (not that we would want something like that on our web app), users would most likely take a while to randomly click on a bar to see the corresponding treemap. However, users are very likely to either try hovering over a bar to see if doing so will yield anything or just do accidentally so while playing around with the web app in general. Hovering also requires less interactions (just moving the mouse over to where the bar(s) is, does not include the additional clicking interaction).

For the bar graph’s interactions, we decided to keep it simple. Bars appear smoothly when new data is given, bars adjust accordingly when data is edited, and bars disappear smoothly when data exits. We were thinking on how to keep the visualization pleasant to the eye while still having a “video game” feel. We compromised by keeping the animations smooth, to-the-point, and pleasant to the eye and changed the general font of the website to a modest “video-gamey” font. 

# Overview of developmental process
 
Describe how the work was split among the team members. Include a commentary on the development process, including answers to the following questions: Roughly how much time did you spend developing your application (in people-hours)? What aspects took the most time?

The work is split equally. Here are the lists of tasks that each member contributed to:

- <u>Eric</u>: bar graph implementation, filter implementation, x-axis rescaling, bar graph animation
- <u>Vic</u>: treemap implementation, tooltip, legend implementation, color scheme, font, treemap animation

Work was mostly done independently through pushing code to either the main branch or a side branch and merged via a pull request. We had meetings at least every 2 days to 1) catch up and update each other on one another’s progress and 2) see if either one of us were having difficulty with a certain feature or had a bug they could not solve quickly. If this was the case, we both spent time looking at the code base to see if either one of us could spot the bug/figure out how to implement the feature together. 

Roughly how much time did you spend developing your application (in people-hours)?
- Around 2-3 hours to discuss the specifications and decide on design decisions
- Around 12 hours to actually implement and iterate the web app
- Around 1 ½ hours to write the write up. 

What aspects took the most time?   
- <u>Treemap implementation.</u> I spent some time understanding how to pass data into the treemap. In the end, I need to aggregate the data into a specific form before passing it into the treemap.
- <u>Bar graph debugging.</u> At first, the bar graph was vertical, and there was a bug where sometimes the bars went below the x-axis before shrinking back. We discovered later the y attributes of the bars change before the height, which is made into animation, chage. However, in the end, we turned the bars vertical in accordance with the feedback, so the bug was not a case we ended up having to worry about at this point.