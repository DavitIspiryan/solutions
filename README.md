# solutions
def setupInitMoney():
    while True:
        money = input("Insert the initial balance above 0: ")
        try:
            money = float(money)
            break
        except ValueError:
            print("Please try again, you probabl have entered not number")
    return money




def setupYears():
    while True:
        years = input("Insert the years above 0: ")
        try:
            years = int(years)
            if years <= 0:
                print ("try again")
                continue
            break
        except ValueError:
            print("Please try again, you probabl have entered not number")
    return years



def setupPercent():
    while True:
        percent = input("Insert the initial percent: ")
        try:
            percent = int(percent)
            if percent <=-1 or percent >=1:
                print ("try again")
                continue
            break
        except ValueError:
            print("Please try again, you probabl have entered not number")
    return percent

def calculateTheResultMoney(money, years, percentage):
    sums = money
    for i in range(years):
        sums = money * (1 + percentage)
    print(" Your inintial money is ", money, ". The result based on",years," and ",percentage," is ",sums)
        

    
def main():
    print("This calculation is for calculating the final loan amount, years, percentage.")
    initMoney = setupInitMoney()
    years =setupYears()
    percent = setupPercent()
    result = calculateTheResultMoney(initMoney, years, percent)
    
main()
