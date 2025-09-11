import random
'''
1 is for snake 
-1 is water 
0 is gun

'''
computer = random.choice([1, -1, 0])
youstr = input("Enter your choice")
youDict = {"s": 1, "w" : -1, "g" : 0  }
reverseDict = { 1 :"snake", -1: "water" , 0: "gun"  }

you = youDict[youstr]

# By now we have 2 numbers (variables), you and computer

print(f"You choose {reverseDict[you]}\nComputer choose {reverseDict[computer]}")

if(computer==you):
    print("Its a Draw")

else:
    if(computer==-1 and you==1 ) :
        print("You Win!")
    elif(computer==-1 and you==0):
        print("You lose!")    
    elif(computer==1 and you==-1):
        print("You lose!")    
    elif(computer==1 and you==0):
        print("You Win!")    
    elif(computer==0 and you==-1):
        print("You Win!")    
    elif(computer==0 and you==1):
        print("You lose!") 

    else:
        print("Something went wrong!")       
