# math-game
import random

c = input('choose game difficulty: easy (1), medium (2), hard (3): ')
k = 0


def easy():
    global k
    x = random.randint(1, 10)
    y = random.randint(1, 10)

    print(x, '+', y, '=', '?')
    z = (input('answer is '))
    if int(z) == x + y:
        k += 1
        print('well done, you have', k, 'points')
    elif int(z) != x + y:
        k -= 1
        print('incorrect answer, you have', k, 'очков')
    else:
        print('entered invalid symbol')


def medium():
    global k
    x = random.randint(1, 100)
    y = random.randint(1, 100)

    print(x, '+', y, '=', '?')
    z = (input('answer is '))
    if int(z) == x + y:
        k += 1
        print('well done, you have', k, 'points')
    elif int(z) != x + y:
        k -= 1
        print('incorrect answer, you have', k, 'points')
    else:
        print('entered invalid symbol')


def hard():
    global k
    x = random.randint(1, 1000)
    y = random.randint(1, 1000)

    print(x, '+', y, '=', '?')
    z = (input('answer is '))
    if int(z) == x + y:
        k += 1
        print('well done, you have', k, 'points')
    elif int(z) != x + y:
        k -= 1
        print('incorrect symbol', k, 'points')
    else:
        print('entered invalid symbol')


while True:

    if c.lower() == '1':
        easy()
    elif c.lower() == '2':
        medium()
    elif c.lower() == '3':
        hard()
    else:
        print('entered invalid symbol')
