def count_digits(n):
    if n < 10:
        return 1
    else:
        return 1 + count_digits(n // 10)

def find_max(numbers):
    if len(numbers) == 0:
        return 0
    elif len(numbers) == 1:
        return numbers[0]
    else:
        mid = len(numbers) // 2
        max1 = find_max(numbers[:mid])
        max2 = find_max(numbers[mid:])
        return max1 if max1 > max2 else max2

def count_tags(html, tag):
    open_tag = "<" + tag + ">"
    close_tag = "</" + tag + ">"
    count = 0
    start_index = html.find(open_tag)
    if start_index != -1:
        end_index = html.find(close_tag, start_index)
        if end_index != -1:
            count = 1 + count_tags(html[end_index + len(close_tag):], tag)
    return count

def display_menu():
    print("1. Count Digits")
    print("2. Find Max")
    print("3. Count Tags")
    print("4. Exit")

def get_choice():
    choice = input("Enter a choice: ")
    return choice

def handle_choice(choice):
    if choice == "1":
        num = int(input("Enter an integer: "))
        count = count_digits(num)
        print("Number of digits:", count)
    elif choice == "2":
        numbers = input("Enter a list of integers (space-separated): ").split()
        numbers = [int(num) for num in numbers]
        max_num = find_max(numbers)
        print("Maximum number:", max_num)
    elif choice == "3":
        html = '''
        <html>
        <head>
        <title>My Website</title>
        </head>
        <body>
        <h1>Welcome to my website!</h1>
        <p>Here you'll find information about me and my hobbies.</p>
        <h2>Hobbies</h2>
        <ul>
        <li>Playing guitar</li>
        <li>Reading books</li>
        <li>Traveling</li>
        <li>Writing cool h1 tags</li>
        </ul>
        </body>
        </html>
        '''
        tag = input("Enter a tag: ")
        count = count_tags(html, tag)
        print("Occurrences of", tag, "tag:", count)
    elif choice == "4":
        print("Exiting the program...")
        return False
    else:
        print("Invalid choice. Please try again.")

    return True

def main():
    running = True
    while running:
        display_menu()
        choice = get_choice()
        running = handle_choice(choice)

if __name__ == "__main__":
    main()
