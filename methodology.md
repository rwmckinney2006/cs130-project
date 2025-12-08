# **Methodology**

## Data Source
* Data was found from an[ NFL Injury Analysis](https://github.com/sammieerne/NFL-Injury-Analysis/blob/af8f7c5f95f21eb9f5504dba73fea8992b69268e/Data/game_injury_player_2019_2020_complete_update_vegas_weeks_bucketed_lower_body.csv) Github Repository

## Data Preparation/Cleaning
* Imported pandas, numpy and matplotlib.pyplot 
* Renamed `num_injuries` column to `num_past_injuries`
* Created a new string column `stadium_type` by defining a function `dome_column_replace` and applying it to `dome` column
* Created a new integer column `total_pts` by adding values from columns `pts_w` and `pts_l`
* Created a new string column `home_or_away` by defining a function `injuries_by_home_or_away` and applying it to the columns `injured_team`, `home_team` and `away_team`
* Defined a function `avg_position_injury_weight` to define a dictionary `avg_weight` and show average injury weight by position.
* Created a new integer column `avg_position_weight` by defining a function `avg_position_weight` and applying it to the column `position`

## Assumptions
* `num_injuries` column was interpreted as the number of past injuries the player has had before the injury recorded in the dataset.
* `weight` column was interpreted to be represented in Pounds(lbs)
* `height` column was interpreted to be represented in Inches(in)
* `avg_temp` column was interpreted to be represented in  Degree Fahrenheit

## Limitations
* Average weight data was not available from 2019/2020 seasons to correspond with dataset, so most recent data available was used
* `num_past_injuries` column does not include data on how recent injury occured which could play a role in analysis
* Two seasons may not be enough data to show clear trends in how attributes affect injury rate
* Whether injury was season ending data was not given