'''
1 for snake 
-1 for water 
0 for gun 
'''
import random
computer = random.choice([-1,0,1])                                       # choice a random number 
print("Choice Your Game Word (W , G , S)")
youstr = input("Enter your choice:")                                    # emter you choice
youDict = {"s":1, "w":-1, "g":0}                                        # change tp value string to dictonary 

reverseDict = { 1:"Snake" , -1:"Water ", 0:"Gun"}                       # reverse to main value 
you = youDict[youstr]

print(f"you  chose:>{reverseDict[you]}\ncomputer chose :>{reverseDict[computer]}")    #choice finding need to game in use reversedict

if(computer == you):                                                     # both chose same 
    print("its a game drow")                

else:
    if(computer == -1 and you == 1):                                                
        print("YOU WIN!")
    elif(computer == -1 and you == 0):
        print("YOU LOSS!")
    elif(computer == 1 and you == -1):
        print("YOU LOSS!")
    elif(computer == 1 and you == 0):
        print("YOU WIN!")
    elif(computer == 0 and you == -1):
        print("YOU WIN!")
    elif(computer == 0 and you == 1):
        print("YOU LOSS!")

    else:
        print("something went worng!")                  # w,s,g not slect the user then output are else condiction " something wenty worng "
