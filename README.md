zasobnik_mleko = 300
zasobnik_kava = 150
zasobnik_voda = 300
cena_espresso = 20
cena_latte = 35
cena_capuccino = 40



while True:
    request = input("Co by jste si dal? (espresso / latte / cappuccino)?")
    if request == "espresso":
        print("Vybrali jste si Esspresso. Cena jednoho Espressa je " + str(cena_espresso))
        money = int(input("Jakou mincí si přejete zaplatit? (1,2,5,10,20,50)"))
        while money < cena_espresso:
            print("To je stále málo, přidej " + str(cena_espresso - money))
            money1 = int(input("Jakou mincí si přejete zaplatit? (1,2,5,10,20,50)"))
            money = money + money1
            continue
        mleko = zasobnik_mleko - 50
        kava = zasobnik_kava - 20
        voda = zasobnik_voda - 30
        
        print("Vaše káva se připravuje :)")

    elif request == "latte":
        print("Vybrali jste si Latte. Cena jednoho Lattéčka je " + str(cena_latte))
        money = int(input("Jakou mincí si přejete zaplatit? (1,2,5,10,20,50)"))
        while money < cena_latte:
            print("To je stále málo, přidej " + str(cena_latte - money))
            money1 = int(input("Jakou mincí si přejete zaplatit? (1,2,5,10,20,50)"))
            money = money + money1
            continue
        print("Vaše káva se připravuje :)")


    elif request == "capuccino":
        print("Vybrali jste si Capuccino. Cena jednoho Capuccina je " + str(cena_capuccino))
        money = int(input("Jakou mincí si přejete zaplatit? (1,2,5,10,20,50)"))
        while money < cena_capuccino:
            print("To je stále málo, přidej " + str(cena_capuccino - money))
            money1 = int(input("Jakou mincí si přejete zaplatit? (1,2,5,10,20,50)"))
            money = money + money1
            continue
        print("Vaše káva se připravuje :)")

    elif request == "check":
        print(f"Hodnota zásobníku mléka: {zasobnik_mleko}\nHodnota zásobníku kávy: {zasobnik_kava}\nHodnota zásobníku vody: {zasobnik_voda}")

    else:
        print("Zadaný nápoj neexistuje")
    
    nabidka = input("Chcete další kávu? ano / ne?")
    if nabidka.lower() != "ano":

        break

