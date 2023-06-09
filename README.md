# celebal-assignment--1
import random
def get_choices():
    player_choice = input('enter a choice (rock, paper, scissors) : ')
    options = ['rock','paper','scissors']
    computer_choice = random.choice(options)
    choices = {'player': player_choice, 'computer': computer_choice}

    return choices

# response = get_choices()
# print(response)

def check_win(player, computer):
    print(f'You choose {player}, Computer choose {computer}')
    if player == computer:
        return 'Its a tie!'
    elif player == 'rock':
        if computer == 'scissors':
            return 'rock smashes scissors, you win!'
        else:
            return 'paper covers rock, you lose!'
    elif player == 'paper':
        if computer == 'rock':
            return 'paper covers rock, you win!'
        else:
            return 'scissors cuts paper, you lose!'
    elif player == 'scissors':
        if computer == 'paper':
            return 'scissors cuts paper, you win!'
        else:
            return 'rock smashes scissors, you lose!'


choices = get_choices()
result = check_win(choices['player'],choices['computer'])
print(result)
