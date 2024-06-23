import random

def guess_number_game():
    secret_number = random.randint(1, 100)
    attempts_left = 5
    
    print("Вгадайте число від 1 до 100. У вас є 5 спроб.")

    while attempts_left > 0:
        guess = int(input("Ваше припущення: "))
        
        if guess == secret_number:
            print(f"Вітаємо! Ви вгадали правильне число {secret_number}.")
            return  
        elif guess < secret_number:
            print("Занадто низько.")
        else:
            print("Занадто високо.")
        
        attempts_left -= 1
        if attempts_left > 0:
            print(f"У вас залишилось {attempts_left} спроб.\n")
        else:
            print(f"Вибачте, у вас закінчилися спроби. Правильний номер був {secret_number}.")

if __name__ == "__main__":
    guess_number_game()
