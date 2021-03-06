# FPL wildcard team selector

This package helps you select the best 15 players to choose when playing a wildcard on Fantasy premier league on any given week

  - Selects the best players by analyzing the latest data provided by the fantasy premier league API, and other premier league stats sources
  - creates a visualization of the selected players
  - creates a csv containing detailed stats on all the players available for selection

### Installation

##### Option #1: Using pip

You can install the package using pip by running the following:

```
pip install FPL-wildcard-team-selector
```
##### Option #2: Download from source

Download the source code by cloning the [repository](https://github.com/abdul-gendy/FPL_wildcard_team_selector). Install by navigating to the proper directory and running
```
python setup.py install
```
### Usage
##### import the package
```
import FPL_wildcard_team_selector
```

##### play_wildcard function
This function selects the best 15 players to pick and creates a visualization of the selected players. It takes in the following 4 arguments: 

  - The amount of money that you have available. Check your team value to get an understanding of how much money you have
  - minimum number of minutes that a player needs to have played in the PL this season for him to be considered for selection
  - number of future gameweeks to analyze
  - whether or not you want to account for penalties during the analysis (If False, uses non-penalty stats)

```
FPL_wildcard_team_selector.play_wildcard(money_available=103.7, minimum_number_of_minutes_played=900, number_of_future_games_to_analyze=3, account_for_penalties=True)
```
##### play_wildcard Sample Output

<img src="test/sample_outputs/Team1.PNG" alt="alt text" width="700" height="700">

##### generate_player_stats function
This functions creates a csv containing detailed stats on all the players. It splits the players in the csv based on posistion, and it places the players in every position catergory in order of best pick to worst pick based on the following 3 arguments: 

  - minimum number of minutes that a player needs to have played in the PL this season for him to be added to the csv
  - number of future gameweeks to analyze
  - whether or not you want to account for penalties during the analysis (If False, uses non-penalty stats)

```
FPL_wildcard_team_selector.generate_player_stats(minimum_number_of_minutes_played=900, number_of_future_games_to_analyze=3, account_for_penalties=True)
```
##### generate_player_stats Sample Output

<img src="test/sample_outputs/sample_csv.PNG" alt="alt text" width="1400" height="500">
