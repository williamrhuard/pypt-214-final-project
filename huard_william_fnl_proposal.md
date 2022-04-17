# Data
1. mission_data.csv
This table contains details of cleaning missions for a sample of 10,000 wifi-connected robots
The columns are defined as follows:
 * **robotid**: a unique robot identifier
 * **datetime**: a date string that represents the start time of a mission in GMT
 * **nmssn**: mission number. This information comes from an internal counter on the robot that increments +1 per mission. Be aware that the complete mission history from mission 1 may not be included for each robot (due to missions being run before the robot was connected to wifi or data loss). The max mission number per robot should reflect its total number of missions to date reported to the database.
 * **runm**: this is the time in minutes that the robot spent actually cleaning.
 * **chrgm**: this is the time in minutes that a robot spent charging.
 * **pausem**: this is the time in minutes that a robot spent paused.
 * **outcome**: this is the end status of a mission. "Cncl" indicates that the mission was cancelled by the user. "Stuck" means the robot got stuck on an obstacle, and was not rescued within 90 minutes, so could not return to the dock. "Bat" means the robot's battery grew too low for it to return to the dock. "Ok" means the robot successfully completed cleaning the space and returned to the dock.

2. geo_data.csv
This table contains details of the robot's geographic location.
The columns are defined as follows:
 * **robotid**: unique robot identifier
 * **country_cd**: 2-letter ISO country code
 * **timezone**: robot's timezone (from IANA/Olson database)

# Tasks
Perform data analysis exploring use patterns of the typical robot user per country. Include relevant visualizations where appropriate.
1. Are there geographic differences in robot usage?
2. Address any possible effects of data loss on your findings.