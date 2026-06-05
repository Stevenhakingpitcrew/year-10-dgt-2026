#Zero blocker

def num_check(question):
    
    error = "Please input a number that is more than zero\n"
    while True:
        try:
            
            response = float(input(question))

            if response > 0:
                return(response)
            else:
                print(error)

        except ValueError:
            print(error)

#start

keep_going = ""
while keep_going == "":

#h+w

    width = num_check("width: ")
    length = num_check("length: ")
    cost = num_check("Cost: ")

    #calc
    perimeter = 2* (width + length)
    cost = cost * perimeter

    #output
    print()
    print(f"perimeter:{perimeter} units")
    print(f"cost: ${cost:.2f}")

    #ask
    keep_going = input("press enter to keep going press any other key to quit")
    print()
    print("thanks for using fence cost calc")
