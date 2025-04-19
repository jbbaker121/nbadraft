# nbadraft
2024 NBA Draft Player Guessing Game - A random 2024 NBA Draft Prospect will be generated, and the user will have to guess the player based on the height, former team, and drafted team provided. 

import random

print("One of the draft picks of the 2024 NBA Draft were chosen randomly.")

word = input("Which first round pick am I thinking of? ")

## Dictionary with players' information
players = {
    "Alex Sarr": {"team": "Perth", "nba": "Wizards", "height": 7.1},
    "Zacharie Risacher": {"team": "Bourg", "nba": "Hawks", "height": 6.9},
    "Ron Holland II": {"team": "Ignite", "nba": "Pistons", "height": 6.7},
    "Reed Sheppard": {"team": "Kentucky", "nba": "Rockets", "height": 6.3},
    "Stephon Castle": {"team": "UConn", "nba": "Spurs", "height": 6.5},
    "Tidjane Salaun": {"team": "Cholet", "nba": "Hornets", "height": 6.9},
    "Donovan Clingan": {"team": "UConn", "nba": "Trail Blazers", "height": 7.3},
    "Rob Dillingham": {"team": "Kentucky", "nba": "Timberwolves", "height": 6.1},
    "Zach Edey": {"team": "Purdue", "nba": "Grizzlies", "height": 7.4},
    "Cody WIlliams": {"team": "Colorado", "nba": "Jazz", "height": 6.7},
    "Matas Buzelis": {"team": "Ignite", "nba": "Bulls", "height": 6.8},
    "Nikola Topic": {"team": "Mega MIS", "nba": "Thunder", "height": 6.6},
    "Devin Carter": {"team": "Providence", "nba": "Kings", "height": 6.2},
    "Carlton Carrington": {"team": "Pittsburgh", "nba": "Wizards", "height": 6.4},
    "Kelel Ware": {"team": "Indiana", "nba": "Heat", "height": 7.0},
    "Dalton Knecht": {"team": "Tennessee", "nba": "Lakers", "height": 6.6},
    "Jared McCain": {"team": "Duke", "nba": "76ers", "height": 6.2},
    "Tristan da Silva": {"team": "Colorado", "nba": "Magic", "height": 6.8},
    "JaKobe Walter": {"team": "Baylor", "nba": "Raptors", "height": 6.4},
    "Jaylon Tyson": {"team": "California", "nba": "Cavs", "height": 6.6},
    "Yves Missi": {"team": "Baylor", "nba": "Pelicans", "height": 6.11},
    "AJ Johnson": {"team": "Illawarra Hawks", "nba": "Bucks", "height": 6.5},
    "DaRon Holmes": {"team": "Dayton", "nba": "Nuggets", "height": 6.9},
    "Kyshawn George": {"team": "Miami", "nba": "Wizards", "height": 6.6},
    "Pacome Dadiet": {"team": "Ratiopharm Ulm", "nba": "Knicks", "height": 6.7},
    "Dillon Jones": {"team": "Weber State", "nba": "Thunder", "height": 6.6},
    "Terrence Shannon Jr": {"team": "Illinois", "nba": "Timberwolves", "height": 6.5},
    "Ryan Dunn": {"team": "Virginia", "nba": "Suns", "height": 6.7},
    "Baylor Scheierman": {"team": "Creighton", "nba": "Celtics", "height": 6.6},
    "Isaiah Collier": {"team": "USC", "nba": "Jazz", "height": 6.2},
    "Adem Bona": {"team": "UCLA", "nba": "76ers", "height": 6.9},
    "Jonathan Mogbo": {"team": "San Francisco", "nba": "Raptors", "height": 6.7},
    "Kyle Filipowski": {"team": "Duke", "nba": "Jazz", "height": 7.0},
    "Tyler Smith": {"team": "Ignite", "nba": "Bucks", "height": 6.10},
    "Johnny Furphy": {"team": "Kansas", "nba": "Pacers", "height": 6.9},
    "Juan Nunez": {"team": "Ratiopharm Ulm", "nba": "Spurs", "height": 6.2},
    "Tyler Kolek": {"team": "Maruqette", "nba": "Knicks", "height": 6.2},
    "Bobi Klintman": {"team": "Cairns", "nba": "Pistons", "height": 6.10},
    "Ajay Mitchell": {"team": "UC Santa Barbara", "nba": "Thunder", "height": 6.4},
    "Jaylen Wells": {"team": "Washington State", "nba": "Grizzlies", "height": 6.6},
    "Oso Ighodaro": {"team": "Marquette", "nba": "Suns", "height": 6.9},
    "KJ Simpson": {"team": "Colorado", "nba": "Hornets", "height": 6.1},
    "Pelle Larsson": {"team": "Arizona", "nba": "Heat", "height": 6.5},
    "Nikola Djurisic": {"team": "KK Mega Bemax", "nba": "Hawks", "height": 6.8},
    "Jamal Shead": {"team": "Houston", "nba": "Rockets", "height": 6.3},
    "Cam Christie": {"team": "Minnesota", "nba": "Clippers", "height": 6.5},
    "Antonio Reeves": {"team": "Kentucky", "nba": "Pelicans", "height": 6.6},
    "Harrison Ingram": {"team": "UNC", "nba": "Spurs", "height": 6.6},
    "Tristen Newton": {"team": "UConn", "nba": "Pacers", "height": 6.4},
    "Enrique Freeman": {"team": "Akron", "nba": "Pacers", "height": 6.8},
    "Melvin Ajinca": {"team": "Saint Quentin", "nba": "Mavs", "height": 6.5},
    "Quinten Post": {"team": "Boston College", "nba": "Warriors", "height": 7.1},
    "Cam Spencer": {"team": "UConn", "nba": "Pistons", "height": 6.3},
    "Anton Watson": {"team": "Gonzaga", "nba": "Celtics", "height": 6.8},
    "Kevin McCullar": {"team": "Kansas", "nba": "Knicks", "height": 6.6},
    "Bronny James": {"team": "USC", "nba": "Lakers", "height": 6.2},
    "Ariel Hukporti": {"team": "MHP Riesen", "nba": "Knicks", "height": 6.10},
    "Ulrich Chomche": {"team": "NBA Academy Africa", "nba": "Raptors", "height": 6.10},
}
player = random.choice(list(players.keys()))

## If/Then Statement to allow user to guess the plauyer based on new provided information for every wrong guess
if word == player:
    print("You guessed it right on your first try!")
else:
    plyr_team = players[player]["team"]
    plyr_height = players[player]["height"]
    plyr_nba = players[player]["nba"]
    print(f"That's not the player I was thinking of. This player is {plyr_height} feet tall.")


    play_again = input("Try again. What is your guess now? ")

    if play_again == player:
        print("You guessed it right after 2 tries.")
    else:
        print(f"That's not the player I was thinking of. This player plays for {plyr_nba}. ")
        play_another = input("What is your guess now? ")
        if play_another == player:
            print("Congrats! You got it right on your third try.")
        else:
            print(f"That is incorrect. This player played for {plyr_team}.")
            play_last = input("Who is your final guess? ")
            if play_last == player:
                print("Congrats! You got it right on your fourth try.")
            else:
                print(f"That is incorrect. The player was {player}. Better luck next time.")
                
