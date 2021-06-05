import random

print("H A N G M A N")
while True:
    modus = input('Type "play" to play the game, "exit" to quit: ')
    if modus == "exit":
        exit()
    elif modus == "play":
        word = random.choice(['python', 'java', 'kotlin', 'javascript'])
        word_lenght = len(word)
        hang_word = "-" * word_lenght
        zeahler = 0
        index = 0
        counter = 0
        counter2 = 0
        list_letters = []
        while zeahler <= 7:
            print(f"\n{hang_word}")
            letter = input("Input a letter: ")
            if len(letter) != 1:
                print("You should input a single letter")
                continue
            if not letter.isalpha() or not letter.islower():
                print("Please enter a lowercase English letter")
                continue
            if letter not in list_letters:
                list_letters.append(letter)
                if letter in word:
                    counter = word.count(letter)
                    for i in range(counter):
                        index = word.find(letter, counter2)
                        hang_word = hang_word[:index] + letter + hang_word[index + 1:]
                        counter2 = index + 1
                else:
                    print("That letter doesn't appear in the word")
                    zeahler += 1
            else:
                print("You've already guessed this letter")

            if hang_word == word:
                break

            counter2 = 0

        if hang_word == word:
            print(f"""\n{word}
You guessed the word!
You survived!\n""")
        else:
            print("You lost!\n")
    else:
        continue
