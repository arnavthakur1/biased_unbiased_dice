# biased_unbiased_dice
Dice game with both biased and unbiased modes.
import random
mode=input("press U for unbiased and B for biased: ")
if mode=='U':
  score=0

  rolls=int(input("enter the number of rolls: "))

  for i in range(1,rolls+1):
    choises=[1,2,3,4,5,6,]
    dice=random.choice(choises)
    print(i,"st roll dice got: ",dice)
    score=score+dice
  print("total score is: ",score)
if mode=='B':
 score=0
 num=int(input("enter the biased number: "))
 if  num<1 or num>6:
    print("enter number from 1 to 6")
 else:
  rolls=int(input("enter the number of rolls: "))
  score=0
  for i in range(1,rolls+1):
    choises=[1,2,3,4,5,6,num,num,num,num,num,num,num]
    dice=random.choice(choises)
    print(i,"st roll dice got: ",dice)
    score=score+dice
  print("total score is: ",score)
if mode!='U' and mode!='B':
    print("enter valid input")
