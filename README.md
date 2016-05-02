# rpg-dice-roller
an rpg dice roller written in python
This is my first coding project. I've been playing dnd lately and it inspired me to write a dice rolling program.
Not that it's easier or faster or more fun than rolling dice, but it gave a me a good idea as a jumping off point to start working on my own projects. 

from random import randint

count = 1 #initialize a count. start at 1 for more intuitive print results
#get input for number of dice and sides
userRoll = input("Enter number and sides of dice like so: xdy. x is number of dice and y is number of sides: ")
dice_total = 0 #initilaze dice_total

#turn input into a list and store each index as a variable
results = userRoll.split("d")
results = [int(i) for i in results]
print(results) #print for testing
                
dice_num = results[0] #sets variable for number of dice
dice_sides = results[1] #sets variable for number of sides

print(dice_num) #bug testing
print(dice_sides) #bug testing

while True:
    dice_sides = results[1] #sets dice_sides to equal number of sides every loop.
    dice_sides = randint(1,dice_sides) #assigns the random number
    
    
    dice_total = dice_total + dice_sides
    print("Die", count, "is:", dice_sides) #prints the result of each die
    print(dice_sides) #bug testing
    count += 1 #increment the counter
    
    #checks if all dice have been "rolled." If so, prints total and ends loop. if not, runs loop again
    if count >= dice_num + 1: 

        print("And the total is:", dice_total)
        break
    
