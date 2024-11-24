# Игра рестики-нолики
player1 = input('Игрок 1, выберите X или O:')
player2 = None
if player1 == 'X':
    player2 = 'O'
elif player1 == 'O':
    player2 = 'X'
else: print('ОШИБКА: Введён неверный символ.')

field = list(range(1, 10))
print((f'{'-------------'}\n'
       f'| {field[0]} | {field[1]} | {field[2]} |\n'
       f'{'-------------'}\n'
       f'| {field[3]} | {field[4]} | {field[5]} |\n'
       f'{'-------------'}\n'
       f'| {field[6]} | {field[7]} | {field[8]} |\n'
       f'{'-------------'}\n'))

for move in range(1, 8):
    move = int(input('Игрок 1, куда поставим X ?:'))
    field[move - 1] = 'X'
    print((f'{'-------------'}\n'
        f'| {field[0]} | {field[1]} | {field[2]} |\n'
        f'{'-------------'}\n'
        f'| {field[3]} | {field[4]} | {field[5]} |\n'
        f'{'-------------'}\n'
        f'| {field[6]} | {field[7]} | {field[8]} |\n'
        f'{'-------------'}\n'))

    move = int(input('Игрок 2, куда поставим O ?:'))
    field[move - 1] = 'O'
    print((f'{'-------------'}\n'
        f'| {field[0]} | {field[1]} | {field[2]} |\n'
        f'{'-------------'}\n'
        f'| {field[3]} | {field[4]} | {field[5]} |\n'
        f'{'-------------'}\n'
        f'| {field[6]} | {field[7]} | {field[8]} |\n'
        f'{'-------------'}\n'))

if field[0] == field[1] == field[2]:
    print('Победа.')
elif field[3] == field[4] == field[5]:
    print('Победа.')
elif field[6] == field[7] == field[8]:
    print('Победа.')
elif field[0] == field[3] == field[6]:
    print('Победа.')
elif field[1] == field[4] == field[7]:
    print('Победа.')
elif field[2] == field[5] == field[8]:
    print('Победа.')
elif field[0] == field[4] == field[8]:
    print('Победа.')
elif field[2] == field[4] == field[6]:
    print('Победа.')
else:
    print('Ничья.')
