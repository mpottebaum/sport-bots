### ENDPOINTS

## AuthController

# LOGIN:

POST /api/v1/auth

Expected Response:

{
    "team": {
        "id": number,
        "name": string,
        "email": string,
        "saved_roster": bool
    },
    "token": string
}


# VERIFY TOKEN

GET /api/v1/auth

Expected Response:

{
    "team": {
        "id": number,
        "name": string,
        "email": string,
        "saved_roster": bool
    },
}


## TeamsController

# CREATE TEAM

POST /api/v1/teams

Expected Response:

{
    "team": {
        "id": number,
        "name": string,
        "email": string,
        "saved_roster": bool
    },
    "token": string
}


# UPDATE TEAM

PUT /api/v1/teams/:id

Expected Response:

{
    "team": {
        "id": number,
        "name": string,
        "email": string,
        "saved_roster": bool
    },
}


## RostersController

# CREATE/READ/UPDATE ROSTER

POST /api/v1/teams/:id/rosters

GET /api/v1/teams/:id/rosters

PUT /api/v1/teams/:id/rosters


Expected Response From Each Endpoint:

{
    "team": {
        "id": number,
        "name": string,
        "email": string,
        "saved_roster": bool
    },
    "roster": {
        "id": number,
        "starters": [
            {
                "id": number,
                "team_id": number,
                "name": string,
                "speed": number,
                "strength": number,
                "agility": number,
            }
        ],
        "alternates": [
            {
                "id": number,
                "team_id": number,
                "name": string,
                "speed": number,
                "strength": number,
                "agility": number,
            }
        ]
    }
}



# DELETE ROSTER

DELETE /api/v1/teams/:id/rosters

Expected Response:

{
    "team": {
        "id": number,
        "name": string,
        "email": string,
        "saved_roster": false
    }
}


# RANDOM ROSTER

GET /api/v1/teams/:id/rosters/random

Expected Response:

{
    "roster": {
        "id": number,
        "starters": [
            {
                "id": number,
                "team_id": number,
                "name": string,
                "speed": number,
                "strength": number,
                "agility": number,
            }
        ],
        "alternates": [
            {
                "id": number,
                "team_id": number,
                "name": string,
                "speed": number,
                "strength": number,
                "agility": number,
            }
        ]
    }
}


## BotsController

# GET TEAM'S BOTS

GET /api/v1/teams/:id/bots

Expected Response:

{
    "bots": [
        {
            "id": number,
            "team_id": number,
            "name": string,
            "speed": number,
            "strength": number,
            "agility": number,
        }
    ]
}