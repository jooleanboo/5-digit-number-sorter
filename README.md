# 5-digit-number-sorter
a program that accepts a five-digit number and sorts its digits based on a given condition. youll find out nalang yung condition lol

    jessePink = int(input("Enter a 5-digit number: "))

    if 10000 <= jessePink <= 99999:

    babyBlue = []

    walterWhite = jessePink
    while walterWhite > 0:
        digit = walterWhite % 10
        babyBlue.insert(0, digit)
        walterWhite = walterWhite // 10

    first_digit = babyBlue[0]

    result_list = []

    if first_digit < 5:
        while len(babyBlue) > 0:
            smallest = babyBlue[0]
            for i in babyBlue:
                if i < smallest:
                    smallest = i
            result_list.append(smallest)
            babyBlue.remove(smallest)

    else:
        while len(babyBlue) > 0:
            largest = babyBlue[0]
            for i in babyBlue:
                if i > largest:
                    largest = i
            result_list.append(largest)
            babyBlue.remove(largest)

    print(f'Sorted number list: {result_list}')

    else:
        print("Invalid input. Please enter exactly five digits.")
