# **Indian-Railways-Data**

## Introduction
This repository contains three JSON files that store information about Indian Railways trains and stations. The three files are:

- **`'trains_dict.json'`**
- **`'station_dict.json'`**
- **`'schedules_dict.json'`**

## `trains_dict.json`
This file contains information about each train including its name, starting station, destination station, pair train, duration, distance, running days, and the stations it passes through. The data is stored as a dictionary with the train number as the key and the rest of the information as the value.

An example of the data is as follows:
```
{
    "10103": {
        "Train_name": "MANDOVI EXPRESS",
        "From_station": "C SHIVAJI MAH T",
        "To_station": "MADGAON",
        "Pair": "10104",
        "Duration": "12:00",
        "Distance": 765,
        "Runs_on": {
            "mon": 1,
            "tue": 1,
            "wed": 1,
            "thu": 1,
            "fri": 1,
            "sat": 1,
            "sun": 1
        },
        "Stations": [
            "CSMT",
            "DR",
            "TNA",
            "PNVL",
            "MNI",
            "KHED",
            "CHI",
            "SGR",
            "RN",
            "ADVI",
            "RAJP",
            "VBW",
            "KKW",
            "SNDD",
            "KUDL",
            "SWV",
            "PERN",
            "THVM",
            "KRMI",
            "MAO"
        ]
    }
}


```

- **`'Train_name'`**: The name of the train. It is a string.
- **`'From_station'`**: The starting station of the train. It is a string.
- **`'To_station'`**: The destination station of the train. It is a string.
- **`'Pair'`**: The train number of the pair train that runs in the opposite direction. It is a string of 4 digits.
- **`'Duration'`**: The duration of the journey in hours and minutes. It is a string in the format "HH:MM".
- **`'Distance'`**: The total distance of the journey in kilometers. It is an integer.
- **`'Runs_on'`**: A dictionary indicating the days on which the train runs. It is a dictionary with 7 keys representing the days of the week and values indicating whether the train runs on that day (1) or not(0).
- **`'Stations'`**: A list of all the stations the train passes through in order. It is a list of strings.
    
    
## `schedules_dict.json`
This file contains information about the schedules of each train including arrival time, departure time, halt time, distance, and day of the journey. The data is stored as a dictionary with the train number as the key and a nested dictionary with the station name as the key and the rest of the information as the value.

An example of the data is as follows:

```

{
    "10103": {
        "CSMT": {
            "Serial_No": 1,
            "Station Name": "C SHIVAJI MAH T",
            "Route Number": 1,
            "Arrival Time": "--",
            "Departure Time": "07:10",
            "Halt Time(In minutes)": "--",
            "Distance": 0,
            "Day": 1
        },
        "DR": {
            "Serial_No": 2,
            "Station Name": "DADAR",
            "Route Number": 1,
            "Arrival Time": "07:22",
            "Departure Time": "07:25",
            "Halt Time(In minutes)": "03:00",

 ```
- **`' Serial_No'`**: The serial number of the station in the train's journey.
- **`'Station Name'`**: The name of the station.
- **`'Route Number'`**: The route number of the train in which the train stops at the station.
- **`'Arrival Time'`**: The arrival time of the train at the station.
- **`'Departure Time'`**: The departure time of the train from the station.
- **`'Halt Time'`**: The time the train spends at the station.
- **`'Distance'`**: The distance from the starting station of the train.
- **`'Day'`**: The day of the journey.

## `stations_dict.json`

This file stores information about Indian railway stations and the trains that pass through them. The data is stored in a dictionary format where each key is a unique station code and the corresponding value is another dictionary containing information about the station.

An example of the data is as follows:

```
{
  "CSMT": {
    "Station_name": "C SHIVAJI MAH T",
    "Trains": [
      "10103", "10104", "11007", "11008", "11009", "11010", "11019",
      "11020", "11029", "11030", "11057", "11058", "11139", "11140",
      "11301", "11302", "11401", "11402", "12051", "12052", "12071",
      "12072", "12105", "12106", "12109", "12110", "12111", "12112",
      "12115", "12116", "12123", "12124", "12125", "12126", "12127",
      "12128", "12133", "12134", "12137", "12138", "12139", "12140",
      "12187", "12188", "12261", "12262", "12289", "12290", "12321",
      "12322", "12361", "12362", "12533", "12534", "12701", "12702",
      "12809", "12810", "12859", "12860", "12869", "12870", "16331",
      "16332", "16339", "16340", "16351", "16352", "17057", "17058",
      "17411", "17412", "17617", "17618", "22105", "22106", "22107",
      "22108", "22119", "22120", "22143", "22144", "17611", "20111",
      "22157", "22159", "22177", "22221", "22731", "17612", "20112",
      "22158", "22160", "22178", "22222", "22732"
    ]
  },
  "DR": {
    "Station_name": "DADAR",
    "Trains": [
      "10103", "10104", "11003", "11004", "11005", "11006", "11007",
      "11008", "11009", "11010", "11019", "11020", "11021", "11022",
      "11027", "11028", "11029", "11030", "11035", "11036", "11041",
      "11042", "11057", "11058", "11139", "11140", "11301", "11302",
     

  ...
}
```
- **`'Station_Code'`**: The code of the station the train passes through.
- **`'Station Name'`**: The name of the station.
- **`'Trains'`**: List of trains running through the station.
