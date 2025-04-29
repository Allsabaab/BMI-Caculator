Dict = {}

while True:
    print("""
Welcome to the BMI Calculator and Tracker""")
    Unit= input("""In which unit do you want to calculate?
Type '1' if in Kg/m^2, type '2' if in lb/ft^2 : """).strip()
    if Unit == "1":
        a = input("Your Name : ").strip()
        b = int(input("Your Age : "))
        c = float(input("Your Weight(in KG) : "))
        d = float(input("Your Height(in M) : "))
        bmi = c / (d * d)
        bmi2f = f"{bmi:.2f}"
        if b < 18:
            print(f"""
{a}, you are not an Adult.
Your BMI is = """ + bmi2f, )
            if bmi < 18:
                print("And you need to gain some weight.")
            elif bmi > 25:
                print("And you need to loose some weight.")
            else:
                print("And you are totally NORMAL.")
        else:
            print(f"""
{a}, you are an Adult.
Your BMI is = """ + bmi2f)
            if bmi < 18:
                print("And you need to gain some weight.")
            elif bmi > 25:
                print("And you need to loose some weight.")
            else:
                print("And you are totally NORMAL.")

        e = input("""
Do you want to save your data?
Type '1' if YES, type '2' if NO or type '3' to recalculate : """).strip()

        if e == "1":
            numb = input("Last two digits of your Phone Number : ").strip()
            Dict[numb] = {a: bmi2f}
            print("Your data has been saved.")
        elif e == "2":
            print("Data not saved.")

        if e == "1":
            f = input("""
Do you want to retrieve your data?
Type '1' if YES or type '2' if NO : """).strip()
            if f == "1":
                data = input("Enter the last two digits of your Phone Number : ").strip()
                if data in Dict:
                    name = list(Dict[data].keys())[0]
                    bmi_value = Dict[data][name]
                    print(f"""
Your Name is {name} and your BMI is {bmi_value}""")
                else:
                    print("No data found for this Phone Number.")

    else:
        a = input("Your Name : ").strip()
        b = int(input("Your Age : "))
        c = float(input("Your Weight(in Pound) : "))
        print("Your Height(in ft) ---")
        m = int(input("      Feet : "))
        n = float(input("      inches : "))
        o = (m*12)+n

        bmi = (c * 703) / (o * o)
        bmi2f = f"{bmi:.2f}"

        if b < 18:
            print(f"""
{a}, you are not an Adult.
Your BMI is = """ + bmi2f, )
            if bmi < 18:
                print("And you need to gain some weight.")
            elif bmi > 25:
                print("And you need to loose some weight.")
            else:
                print("And you are totally NORMAL.")
        else:
            print(f"""
{a}, you are an Adult.
Your BMI is = """ + bmi2f)
            if bmi < 18:
                print("And you need to gain some weight.")
            elif bmi > 25:
                print("And you need to loose some weight.")
            else:
                print("And you are totally NORMAL.")

        e = input("""
Do you want to save your data?
Type '1' if YES, type '2' if NO or type '3' to recalculate : """).strip()

        if e == "1":
            numb = input("Last two digits of your Phone Number : ").strip()
            Dict[numb] = {a: bmi2f}
            print("Your data has been saved.")
        elif e == "2":
            print("Data not saved.")

        if e == "1":
            f = input("""
Do you want to retrieve your data?
Type '1' if YES or type '2' if NO : """).strip()
            if f == "1":
                data = input("Enter the last two digits of your Phone Number : ").strip()
                if data in Dict:
                    name = list(Dict[data].keys())[0]
                    bmi_value = Dict[data][name]
                    print(f"""
Your Name is {name} and your BMI is {bmi_value}""")
                else:
                    print("No data found for this Phone Number.")

    g = input("""
Do you want to calculate another BMI?
Type '1' if YES or type '2' if NO : """).strip()
    if g == "2":
        print("Goodbye!")

        break
