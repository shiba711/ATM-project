# ATM-project
This ATM project is written using function in python 

pin=1234
balance=20000
print("Welcome To SBI Bank ")
validation()

def validation():
    upin=int(input("Enter your pin : ")) 
    if(upin==pin):
        menu(balance)
    else:
        a=1
        while(a<3):
            a=a+1
            upin=int(input("Re-enter pin : "))
            if(upin==pin):
                menu(balance)
        else:
            print("card blocked")
                

def menu(balance):
    print("enter 1 for balance")
    print("enter 2 for withdraw")
    print("enter 3 for deposit")
    print("enter 4 for pin change")
    print("enter 0 to EXIT")
    opt=int(input())
    
    while(opt!=0):
        
        if(opt==1):#check balance
            print("Your current balance is ",balance)
            opt=int(input("next option"))
            
        elif(opt==2):#withdraw
            amt=int(input("Enter amount to withdraw : "))
            balance=balance-amt
            print("balance:Rs.",balance)
            opt=int(input("next option"))
            
        elif(opt==3):#deposit
            amt=int(input("Enter amount to deposit : "))
            balance=balance+amt
            print("balance:Rs.",balance)
            opt=int(input("next option"))
            
        elif(opt==4): 
            pinchange(pin)
            opt=int(input("next option"))
            
        elif(opt==0):
            print("---------------------------")
            print("Thank You for Trasaction")
            print("---------------------------")

        else:
            print("invalid option")
            break

def pinchange(pin):
    print("Enter old pin : ")
    pin=int(input())
    if(pin==pin):
        print("Enter new pin : ")
        pin=int(input())
        print("new pin generated")
    else:
        print("pin not matched")



