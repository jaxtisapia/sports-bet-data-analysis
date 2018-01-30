# SPORTS BET PREDICTION

### Introduction

I've been gathering data of all matches in different leagues in different countries since August 2017 - About 20,000 matches (As at TODAY - 30/01/2018)

As match data keeps adding up automatically, specific bet odds related to the match are also stored
Hidden within this data are lots of precious gems. Already found one of such gems - xD


### Structure of A Bet {Object}

This is a sample bet object before the match(event) is played. Usually collected 24 hours before the match:

```
{
    "_id": 4646588,
    "competition": {
        "id": 2153452,
        "name": "Serie A",
        "weight": 796,
        "category": 2153406
    },
    "event": {
        "start": {
            "$date": "2018-02-10T19:45:00.000Z"
        },
        "name": "SSC Napoli vs SS Lazio"
    },
    "team": {
        "home": "SSC Napoli",
        "away": "SS Lazio"
    },
    "difference": {
        "1_2": 4.25,
        "1_X": 2.9000000000000004,
        "X_2": 1.3499999999999996,
        "1_1X": 0.3799999999999999,
        "2_2X": 3.35,
        "1_12": 0.32000000000000006,
        "2_12": 4.57
    },
    "odds": [
        {
            "type": "MRES",
            "subtype": "X",
            "id": 364295859,
            "status": "NONE",
            "value": 4.4
        },
        {
            "type": "MRES",
            "subtype": "1",
            "id": 364295855,
            "status": "NONE",
            "value": 1.5
        },
        {
            "type": "MRES",
            "subtype": "2",
            "id": 364295865,
            "status": "NONE",
            "value": 5.75
        },
        {
            "type": "OVUN",
            "subtype": "Over",
            "id": 364331309,
            "status": "NONE",
            "value": 1.6
        },
        {
            "type": "OVUN",
            "subtype": "Under",
            "id": 364331313,
            "status": "NONE",
            "value": 2.3
        },
        {
            "type": "DBLC",
            "subtype": "1X",
            "id": 364295797,
            "status": "NONE",
            "value": 1.12
        },
        {
            "type": "DBLC",
            "subtype": "X2",
            "id": 364295804,
            "status": "NONE",
            "value": 2.4
        },
        {
            "type": "DBLC",
            "subtype": "12",
            "id": 364295801,
            "status": "NONE",
            "value": 1.18
        }
    ],
    "score": "",
    "updated": false,
    "added_on": {
        "$date": "2018-01-30T01:01:21.177Z"
    },
    "sport": "SOCCER"
}
```

This is the updated Objected after a match or event is complete

```
{
    "_id": 4796772,
    "competition": {
        "id": 2153968,
        "name": "Football National League",
        "weight": 0.5,
        "category": 2153964
    },
    "event": {
        "start": {
            "$date": "2017-10-29T09:00:00.000Z"
        },
        "name": "FC Tom Tomsk vs Luch-Energia Vladivostok"
    },
    "team": {
        "home": "FC Tom Tomsk",
        "away": "Luch-Energia Vladivostok"
    },
    "difference": {
        "1_2": 1.7500000000000002,
        "1_X": 1.2,
        "X_2": 0.5500000000000003,
        "1_1X": 0.73,
        "2_2X": 1.9500000000000002,
        "1_12": 0.7,
        "2_12": 2.45
    },
    "odds": [
        {
            "type": "MRES",
            "subtype": "2",
            "id": 334438843,
            "status": "LOSE",
            "value": 3.7
        },
        {
            "type": "MRES",
            "subtype": "X",
            "id": 334438842,
            "status": "WIN",
            "value": 3.15
        },
        {
            "type": "MRES",
            "subtype": "1",
            "id": 334438840,
            "status": "LOSE",
            "value": 1.95
        },
        {
            "type": "DBLC",
            "subtype": "12",
            "id": 334438790,
            "status": "LOSE",
            "value": 1.25
        },
        {
            "type": "DBLC",
            "subtype": "1X",
            "id": 334438788,
            "status": "WIN",
            "value": 1.22
        },
        {
            "type": "DBLC",
            "subtype": "X2",
            "id": 334438792,
            "status": "WIN",
            "value": 1.75
        },
        {
            "type": "OVUN",
            "subtype": "Over",
            "id": 334440277,
            "status": "LOSE",
            "value": 2.4
        },
        {
            "type": "OVUN",
            "subtype": "Under",
            "id": 334440283,
            "status": "WIN",
            "value": 1.5
        }
    ],
    "score": "0-0",
    "updated": true,
    "added_on": {
        "$date": "2017-10-22T10:01:12.967Z"
    },
    "sport": "SOCCER"
}
```


### WTF?!?! There's nothing special about this data

YES. There's nothing special about this data. But this data is precious in huge quantities.

Fast Foward. I've been able to make some deductions, which predicts accurately as high as 80% success! However, this only applies to the 'BARCLAYS ENGLAND PREMIER LEAGUE'. Haven't tried modelling for other leagues.

Follow this trend to predict for Barclays Premier League

```
Team A vs Team B
Odds for team A: X
Odds for team B: Y

If X-Y = Between 1 and 2 ------> Team A wins or draws 80% of the time
If Y-X = Between 1 and 2 ------> Team B wins or draws 80% of the time

It's that Simple
```

NOTE: I have no technical background in either betting, or data analysis. I just have access to the data, and I've been able to gather chunks of them


### Contributions

However, you can contribute to this project to make more bet prediction models from the data i have.

I'm willing to give access to the data. But you should be conversant with JSON Data and MongoDb(not necessary though)

Feel free to contact me to contribute.

