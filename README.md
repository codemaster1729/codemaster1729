import random

class Player:
    def __init__(self, name, batting_skill, bowling_skill, fielding_skill):
        self.name = name
        self.batting_skill = batting_skill
        self.bowling_skill = bowling_skill
        self.fielding_skill = fielding_skill

class Match:
    def __init__(self, team1, team2):
        self.team1 = team1
        self.team2 = team2
        self.current_team = team1
        self.current_batsmen = [team1[0], team1[1]]
        self.current_bowler = random.choice(team2)

    def simulate_ball(self):
        # Simulate batting team's decision
        decision = input("What will {} do? (Attack/Defend/Rotate Strike): ".format(self.current_team.name)).lower()
        if decision == "attack":
            # Implement attacking strategy
            pass
        elif decision == "defend":
            # Implement defending strategy
            pass
        elif decision == "rotate strike":
            # Implement rotating strike strategy
            pass
        else:
            print("Invalid decision!")
            self.simulate_ball()

    def play(self):
        print("Match starts between {} and {}".format(self.team1.name, self.team2.name))
        # Match simulation loop
        while True:
            self.simulate_ball()
            # Check match conditions and update accordingly
            # Check for end of match conditions

# Example usage
player1 = Player("Player1", 80, 70, 75)
player2 = Player("Player2", 85, 65, 80)
team1 = [player1, player2]

player3 = Player("Player3", 75, 80, 70)
player4 = Player("Player4", 70, 85, 75)
team2 = [player3, player4]

match = Match(team1, team2)
match.play()

