# Project of Data Visualization (COM-480)

| Student's name | SCIPER |
| -------------- | ------ |
| Alexandre Variengien| 337357 |
| Félicie Giraud-Sauveur| 284220 |
| Assia Ouanaya| 288251 |

[Milestone 1](#milestone-1) • [Milestone 2](#milestone-2) • [Milestone 3](#milestone-3)

## Milestone 1 (23rd April, 5pm)

**10% of the final grade**

This is a preliminary milestone to let you set up goals for your final project and assess the feasibility of your ideas.
Please, fill the following sections about your project.

*(max. 2000 characters per section)*

### Dataset

We chose to work with the ATP Tennis with Betting Odds found on [Kaggle](https://www.kaggle.com/datasets/edoardoba/atp-tennis-data/metadata). 

Description of the dataset:
- ATP: Tournament number
- Location: Venue of tournament
- Tournament: Name of tournament
- Date: Date of match
- Series: Name of ATP tennis series
- Court: Type of court
- Surface: Type of surface
- Round: Round of match
- Best of: Maximum number of sets playable in match
- Winner: Match winner
- Loser: Match loser
- WRank: ATP Entry ranking of the match winner as of the start of the tournament
- LRank: ATP Entry ranking of the match loser as of the start of the tournament
- WPts: ATP Entry points of the match winner as of the start of the tournament
- LPts: ATP Entry points of the match loser as of the start of the tournament
- W1: Number of games won in 1st set by match winner
- L1: Number of games won in 1st set by match loser
- W2: Number of games won in 2nd set by match winner
- L2: Number of games won in 2nd set by match loser
- W3: Number of games won in 3rd set by match winner
- L3: Number of games won in 3rd set by match loser
- W4: Number of games won in 4th set by match winner
- L4: Number of games won in 4th set by match loser
- W5: Number of games won in 5th set by match winner
- L5: Number of games won in 5th set by match loser
- Wsets: Number of sets won by match winner
- Lsets: Number of sets won by match loser
- Comment: Comment on the match (Completed, won through retirement of loser, or via Walkover)
- B365W: Bet365 odds of match winner
- B365L: Bet365 odds of match loser
- PSW: Bet&Win odds of match winner
- PSL: Bet&Win odds of match loser
- MaxW: Maximum odds of match winner
- MaxL: Maximum odds of match loser
- AvgW: Average odds of match winner
- AvgL: Average odds of match loser
- EXW: Expekt odds of match winner
- EXL: Expekt odds of match loser
- LBW: Ladbrokes odds of match winner
- LBL: Ladbrokes odds of match loser
- SJW: Stan James odds of match winner
- SJL: Stan James odds of match loser
- UBW: Unibet odds of match winner
- UBL: Unibet odds of match loser
- pl1_flag: Winners Nationality
- pl1_year_pro: Winners starting year as a pro
- pl1_weight: Winners weight
- pl1_height: Winners height
- pl1_hand: Winners playing hand
- pl2_flag: Losers Nationality
- pl2_year_pro: Losers starting year as a pro
- pl2_weight: Winners weight
- pl2_height: Losers height
- pl2_hand: Losers playing hand

### Problematic

Since its creation in the nineteenth century, tennis has kept increasing in popularity to become one of the most played sports, and one of the most mediatized. You cannot ignore the names of the best figures such as Rafael Nadal or Novak Djokovic that compete in the unmissable Grand Slam tournaments: from Roland Garros to Wellington.
Nonetheless, the usual picture of tennis shared by the media tends to focus on a tiny subset of both the events and the players.
With this visualization, we want to give a holistic image of the community of professional tennis players, its global structure.  

First, we want to visualize the pattern of matchmaking through tournaments and through the seasons. All the tournaments can be seen as a graph whose nodes are the players and the edges are the tennis matches. We want to visualize the structure of this graph.  

In addition to the competitions, we would focus on individual players: besides the well-known superstars, what is the usual career of a professional tennis player, what are his characteristics? We want to share the stories of the ones whose names will never appear in any international headlines, while they make up the biggest chunk of the community.  
Those questions, such as the role of right or left handedness, are the subject of common discussions. Through the use of data visualization, we aim at shedding new light on these topics.  

This visualization is intended for the general public, with no particular interest in tennis. Our goal is to show the fascinating patterns that emerge in the data visualization from this field and to share the statistical stories that never appear in newspapers.

### Exploratory Data Analysis

See jupyter notebook "milestone1.ipynb".

### Related work/Our ideas

These type of data about tennis can be presented in a very classical way in the form of tables detailing the statistics of the players according to different criteria. This is the case for instance on these two reference sites: http://www.tennisabstract.com/cgi-bin/leaders.cgi?f=B0s00o1 or https://www.atptour.com/en/stats.  
There are also much more original ways to present and play with this type of data as can be seen on these two sites of data visualization: https://tennisvisuals.com/ or https://www.nationalgeographic.com/culture/article/150906-data-points-tennis-tracking.
We can also find analyses that already exist on similar data like here: https://www.kaggle.com/code/nescobar/data-visualizations-of-atp-tennis-competitions/notebook.

Our idea is original in the sense that it aims to show much more the links between all players and countries. Our ambitions for the moment are as follows:

- ***Tab 1*: Network between players:**
    - Make a network that connects players who have played a match. Interactivity: you can move the nodes with the mouse to make the network move.
    - A node corresponds to a player (with the picture of the player in the node). The bigger the node, the more matches the player has made. 
    - Slider to choose the year.
    - Buttons to apply filters according to different variables: Location, Tournament, Serie, Court, Surface, Players ranking range.
    - Possibility to mouseover a node (player): information about the player is displayed with for instance the number of matches played in ATP by series per year, the number of wins and the number of losses according to the year/the tournament/the type of court/the type of surface, his nationality, his weight, his year of start as a pro and his playing hand, a list with his main opponents. 
    - It is also possible to mouseover on the edge between two players: information is displayed with the characteristics of the matches. For instance: locations, tournaments, dates, series, courts, surfaces, rounds, winners, ranks and points of the players at the beginning of the tournament, number of games won by each player for each set, number of sets won by each player, comments, odds.
    - Inspirations: http://www.claudiobellei.com/2017/02/04/viznetworks/ ; http://bl.ocks.org/eesur/be2abfb3155a38be4de4 ; https://bl.ocks.org/steveharoz/8c3e2524079a8c440df60c1ab72b5d03 ; https://d3-graph-gallery.com/graph/interactivity_button.html ; https://sylhare.github.io/2020/06/10/Advanced-node-network-graph-d3.html

- ***Tab 2*: World map visualisation:**

    - The goal of this animated visualization is to picture the geographical movement of a tennis player going from tournement to tournement. 
    - Each player is represented by a colored circle on a world map, the movement of the circle follows the cities the player visited during the tournements present in the database.
    - The map will be an [azimuthal equidistant polar projection](https://en.wikipedia.org/wiki/Azimuthal_equidistant_projection) to be able to show movement around the globe with minimal discoutinuosities induced by wraping at the corners.
    -The color of the circles will correspond to the ranking of the player (e.g. the more yellow, the higher rank). This could be useful to visualize the levels of the player present at a given tournament.
    - Inpiration of the visualization (A flow where a colored icon correspond to one person, we added the geographical component): https://www.nytimes.com/interactive/2018/03/19/upshot/race-class-white-and-black-men.html 


- ***Tab 3*: Bart Charts moving over time:**
    - Two bart charts on the same line with the bars moving as the years go by.
    - A first bart chart to show the evolution of the countries ranking in terms of number of wins or points or players etc...
    - A second bart chart to show the evolution of the players in terms of number of wins or points or number of matches etc...
    - Button to apply filters according to different variables: Series, Court, Surface.
    - Inspiration: https://observablehq.com/@d3/bar-chart-race  

- ***Tab 4*: Slot Machine between 2 players (optional, to be implemented if we have time):**
	- The goal would be to implement a slot machine that chooses randomly 2 players and displays statistics about their last matches between these 2 players. 
	- The slot machine would display basic information about the 2 players such as Name, image, nationality and rank. The statitistics shown between the two players are the number of matches played (at least >= 1), the number of wins of the 1st player, at which country and tournament they most played in.
	- You can click on a button "SHUFFLE" that will pick 2 new players. 
	- Some visualization inspiration https://josex2r.github.io/jQuery-SlotMachine/ & https://odhyan.com/slot/.

- ***(Side ideas for the site)***:
    - Make the loading symbol in the form of a spinning tennis ball.
    - Make a mascot in the form of a tennis racket to explain the site's features at the beginning.
    - Make symbols for the selection of variables, a small cup for the winner, flags for the nationalities, etc...

*NB : The dataset is extracted from the Kaggle database [ATP tennis data](https://www.kaggle.com/datasets/edoardoba/atp-tennis-data) and only a "Djokovic vs Nadal quick analysis" is presented as analysis of this data.*


## Milestone 2 (7th May, 5pm)

**10% of the final grade**

### Visualisation Descriptions

#### Tab 1: Network between players

The first visualization will be a network that connects players who have played a match. A node corresponds to a player (with the picture of the player in the node). The bigger the node, the more matches the player has made. Inspiration: http://www.claudiobellei.com/2017/02/04/viznetworks/ and http://bl.ocks.org/eesur/be2abfb3155a38be4de4.

<img src="/img/network.png" alt="network" width="1100"/>

It will be possible to move the nodes with the mouse to make the network move.

<img src="/img/network_moving.png" alt="network_moving" width="200"/>

It will be possible to select some specific data with buttons to apply filters according to different variables. For instance: Location, Tournament, Serie, Court, Surface, Players ranking range... Inspiration: https://d3-graph-gallery.com/graph/interactivity_button.html ; https://bl.ocks.org/steveharoz/8c3e2524079a8c440df60c1ab72b5d03.

<img src="/img/network_choices.png" alt="network_choices" width="200"/>

A slider will also enable to choose the year. Inspiration: http://www.claudiobellei.com/2017/02/04/viznetworks/.

<img src="/img/network_curseur.png" alt="network_curseur" width="300"/>

When we pass the mouse over a node (player), information about the player will be displayed with for instance: the number of matches played in ATP by series per year, the number of wins and the number of losses according to the year/the tournament/the type of court/the type of surface, his nationality, his weight, his year of start as a pro and his playing hand, a list with his main opponents. Inspiration: https://sylhare.github.io/2020/06/10/Advanced-node-network-graph-d3.html.

<img src="/img/network_joueur.png" alt="network_joueur" width="400"/>

When we pass the mouse over the edge between two players, information will be displayed with the characteristics of the matches. For instance: locations, tournaments, dates, series, courts, surfaces, rounds, winners, ranks and points of the players at the beginning of the tournament, number of games won by each player for each set, number of sets won by each player, comments, odds. Inspiration: https://sylhare.github.io/2020/06/10/Advanced-node-network-graph-d3.html.

<img src="/img/network_edge.png" alt="network_edge" width="600"/>

#### Tab 2: World map visualisation

##### Librairies

https://en.wikipedia.org/wiki/Azimuthal_equidistant_projection goal of the projection

http://proj4js.org/ for messing with projection

https://observablehq.com/@d3/azimuthal-equidistant

https://github.com/d3/d3-geo-projection to create the map

https://github.com/d3/d3-geo/blob/main/README.md#geoInterpolate interpolation between different points (the tournaments)

##### Dynamics

-> each point is at the tournament the day of his match. Between two matches, he goes from Tournament A to Tournament B at constant speed.

  
New player appear with a fade in at the first tournament location, disappear after the last match

##### Color
color palette of yellow to white. The more yellow, the high ranked they are (the color change during time, after matches)

  

Add a color scale for mapping color to ranking

##### Map

Location of the tournament added with tags name of the city (+ tournament name, we have to see if we have many tournaments in the same city)

##### Layout

Map in the main screen (see layout of the general website) + a cursor to indicate the date (as in OurWorldInData)

By default, the time is going forward and loops at the end you can displace the cursor to get to a precise time

<img src="/img/map_maquette.png" alt="maquette" width="1200"/>

#### Tab 3: Bar chart race

* Classical bar chart race
* Options :
	 * **Bars** per country / per players
	
	 * **Metrics** Number of victories, number of ATP points (= ranking for players, sum for countries)

Cursor at the bottom to define the time


#### Tab 4: Slot Machine (optional, to be implemented if we have time)

The goal would be to implement a slot machine that chooses randomly 2 players and displays statistics about their last matches between these 2 players. The workflow would be the following:

<img src="/img/slot.png" alt="slot" width="1100"/>

## Milestone 3 (4th June, 5pm)

**80% of the final grade**


## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone
