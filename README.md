import random


rock = '''
    ___
---'   ____)
      (_)
      (_)
      (____)
---.(___)
'''

paper = '''
    ___
---'   )
          __)
          ___)
         ___)
---.__)
'''

scissors = '''
    ___
---'   )
          __)
       __)
      (____)
---.(___)
'''


variantlar = [rock, paper, scissors]
nomi = ["rock", "paper", "scissors"]
print("Rock, Paper, Scissors o'yiniga xush kelibsiz!")
foydalanuvchi_tanlovi = int(input("Quyidagilardan birini tanlang:\n0 - rock\n1 - paper\n2 - scissors\nSizning tanlovingiz (0, 1, 2): "))
if foydalanuvchi_tanlovi < 0 or foydalanuvchi_tanlovi > 2:
    print("Noto'g'ri tanlov! Iltimos, 0, 1 yoki 2 tanlang.")
else:
    
    kompyuter_tanlovi = random.randint(0, 2)
    
    print(f"\nSizning tanlovingiz: {nomi[foydalanuvchi_tanlovi]}")
    print(variantlar[foydalanuvchi_tanlovi])
    
    print(f"Kompyuter tanlovi: {nomi[kompyuter_tanlovi]}")
    print(variantlar[kompyuter_tanlovi])
    

    if foydalanuvchi_tanlovi == kompyuter_tanlovi:
        print("Durrang!")
    elif foydalanuvchi_tanlovi == 0 :
        if kompyuter_tanlovi == 2:   
            print("Siz yutingiz! Rock scissorsni yengadi.")
        else:                         
            print("Kompyuter yuti! Paper rockni yengadi.")
    elif foydalanuvchi_tanlovi == 1: 
        if kompyuter_tanlovi == 0:   
            print("Siz yutingiz! Paper rockni yengadi.")
        else:                        
            print("Kompyuter yuti! Scissors paperni yengadi.")
    elif foydalanuvchi_tanlovi == 2:  
        if kompyuter_tanlovi == 1:    
            print("Siz yutingiz! Scissors paperni yengadi.")
        else:                        
            print("Kompyuter yuti! Rock scissorsni yengadi.")
