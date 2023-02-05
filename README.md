# Indian-Railways-Data

##Introduction
This repository contains three JSON files that store information about Indian Railways trains and stations. The three files are:

-trains_dict.json
-station_dict.json
-schedules_dict.json

##trains_dict.json
This file contains information about each train including its name, starting station, destination station, pair train, duration, distance, running days, and the stations it passes through. The data is stored as a dictionary with the train number as the key and the rest of the information as the value.

The structure of the data is as follows:
'''java
{
    "<Train_Number>": {
        "Train_name": "<Train Name>",
        "From_station": "<Starting Station>",
        "To_station": "<Destination Station>",
        "Pair": "<Pair Train Number>",
        "Duration": "<Duration of the journey>",
        "Distance": <Total Distance>,
        "Runs_on": {
            "mon": <0/1>,
            "tue": <0/1>,
            "wed": <0/1>,
            "thu": <0/1>,
            "fri": <0/1>,
            "sat": <0/1>,
            "sun": <0/1>
        },
        "Stations": [
            "<Station 1>",
            "<Station 2>",
            ...
            "<Station n>"
        ]
    },
    ...
}

'''


Train_Number: The unique identifier for the train. It is a string of 4 digits.
Train_name: The name of the train. It is a string.
From_station: The starting station of the train. It is a string.
To_station: The destination station of the train. It is a string.
Pair: The train number of the pair train that runs in the opposite direction. It is a string of 4 digits.
Duration: The duration of the journey in hours and minutes. It is a string in the format "HH:MM".
Distance: The total distance of the journey in kilometers. It is an integer.
Runs_on: A dictionary indicating the days on which the train runs. It is a dictionary with 7 keys representing the days of the week and values indicating whether the train runs on that day (1) or not (0).
Stations: A list of all the stations the train passes through in order. It is a list of strings.
    
    
##schedules_dict.json
This file contains information about the schedules of each train including arrival time, departure time, halt time, distance, and day of the journey. The data is stored as a dictionary with the train number as the key and a nested dictionary with the station name as the key and the rest of the information as the value.

The structure of the data is as follows:

'''json

{
    "<Train_Number>": {
        "<Station_Name>": {
            "S.N.": <Serial Number>,
            "Station Name": "<Station Name>",
            "Route Number": <Route Number>,
            "Arrival Time": "<Arrival Time>",
            "Departure Time": "<Departure Time>",
            "Halt Time":"<Halt Time in Minutes>",
            "Distance":"<Distance from start station>"
            "Day":"<Day of the journey>"
    }
 }'''
