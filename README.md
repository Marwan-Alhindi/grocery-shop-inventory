# simple program to manage grocery shop inventory
"""
    Made By: Marwan Alhindi
    Created On: 4 Sep 2022
    Finished On: 9 Sep 2022

    Overview:
    This file/assignment is to develop programming and problem solving skills. It introduce concepts such as loops, arrays, and methods.

    [] is used in comments to reference a line.
    {} is used in comments to reference a loop.

    File goals:
    This file is a simple program for a grocery store shop to manage its inventory where an assumption has been made that the user input is always valid. The program file is written to develop the following skills:
    1. Follow coding, convention and behavioral requirements provided in this document and in the lessons.
    2. Independently solve a problem by using programming concepts taught over the first several weeks of the course.
    3. Write and debug Python code independently.
    4. Document code.
    5. Ability to provide references where due.
    6. Meeting deadlines.
    7. Seeking clarification from your “supervisor” (instructor) when needed via discussion forums.
    8. Create a program by recalling concepts taught in class, understanding and applying concepts relevant to solution, analysing components of the problem, evaluating different approaches.
    9. Demonstrate knowledge of basic concepts, syntax and control structures in programming.
    10. Devise solutions to simple computing problems under specific requirements.
    11. Encode the devised solutions into computer programs and test the programs on a computer.
    12. Demonstrate understanding of standard coding conventions and ethical considerations in programming.

    Documentation Style:
    I have used PEP 8 style guide for Python Code. I have also tried to follow PEP 20 - The Zen of Python
    https://peps.python.org/pep-0008/
    https://peps.python.org/pep-0020/ or import this to view in terminal

    What I have learnt:
    1- When you change one word/variable in the program, make sure that you have changed all of them. The shortcut to do this is to select a word/variable and then click F2.
    2- Do not comment and program simultaneously. This will make your thinking about solving an issue harder. Solve the issue logically and then comment how the program flow and the way you solved the issue.
    3- The way you solved majority of issues that you have faced during this project is:
        1- Read the instructions of what you have been asked to do VERY CAREFULLY and asks questions if you dont know exactly the requirements. A single word from the instructions can change what you are supposed to program. Dont just read the instructions one by one, make sure that you read them through all together so that you can understand how the program can be connected.
        2- Naming variables correctly in a way that you can understand can make discovering issues with the program and debug it easier. This is really important because sometimes you tend to forget how you wrote the code.
        3- Check for syntax errors and errors if you are not using the right functions or keywords.
        4- Make sure that the flow of program matches the logic of the problem you are trying to solve. Do you choose if-else or if-if-else or if-elif-else? There are many options to control the flow of the program.
        5- If you think the flow of the program is correct and the issue was not solved, dont just trust your idea of how the program should flow, DEBUG!
    4- Be efficient! When there's a function that you can import from someone else or use, then embrace their work and use it! A really good example of this is when you used isinstance() function.
    5- When you wrap up and stop working on the project, write a docstring at the end of the document to remind you the next time you open the project where you stop at and what you can do next.
    6- It's really important to create versions when you develop a project. Your mind comes with new ideas all the time. You might think the new idea will develop the program but sometimes you dont have the required knowledge to implement it or even if you developed it, the old idea might turn to be better.
    7- To make the code more readable, create functions for any repetitive code.
    8- Seperate functions to the logic of the program. Unfourtantly, you cant do that in this project, but generally speaking its a a good way to make the code more readable.
    9- Dont fall in the trap that finishing a project in one long interval is more efficient, fresh starts brings fresh ideas. Do the project on seperate days.
    10- When you finish the program, write a full story such as the following. This will make sure that you did not miss requirements:
        - Story
    11- To not get lost on what to do, writing list of tasks can help. But also sometimes applying tasks method can make coding harder! An example of this is when you was trying to write the order sumamry for a new purchase:
            # 1- know if customer is old or new to apply discount.
            # 2- get the price of each entered item and store it in a list by using .index method
            # 3- get the quantity of each item and store it in a list.
            # 4- create a price list where the price of each item purchase is item * quantity
            # 5- using the quantity of each item, multiply the quantities with the item unit price and store that in a list
            # 6- sum up the list for the total price.
            # 7- print a statement for the order history
    12- Check the program flow for an if-else inside an if-else in new_purchase function. This is a good program flow. Which condition you should put first? A really good example of this is the if-if-if-if statements in update_products function.
    13- When you construct a while loop, make sure you use the right condition. You can use while flag: or while True:. The difference is that when you use while flag, the flag changes and continue the code then the loop stops. But if you used while True and break, it instantly breaks.
    14- Dont try to fix code when you are tired, you only gonna make it worse.
    15- Print statements can be a really good way to test code and check things working as expected!
    16- If the structure of the basic features are built correctly, adding more complex features can be easier. This is because complex features could be dependant on the basic/initial features. So, make sure you get the basics correctly so that when you develop new features, you dont need to debug the old ones often.
    17- You can go to a line instantly by using the following shortcut: Ctrl+G and then type the line number.
    18- Make sure that you first understood the task clearly and then create an algorithm that make sense with the task. If you didnt understand the task clearly, you will write code that is wasted. An example where you did this is when you tried to create the table of most valuable customer:
        each_item_totalPrice = product_history.copy()
        for i in range(len(product_history)):
            for j in range(len(product_history[i])):
                single_item = product_history[i][j]
                single_item_index = products_glob.index(single_item)
                single_item_price = float(prices_glob[single_item_index])
                one_quantity = float(quantity_history[i][j])
                each_item_totalPrice[i][j] = single_item_price*one_quantity
        print(each_item_totalPrice)
    19- When you create list of lists make sure you do it the right way because if you didnt, each item in the list of lists might have the same id and so you cant change each item by itself. You can use the function id() to check the reference
    20- To iterate through two lists at the same time, use zip() function:
        for product,quantity in zip(product_list,quantity_list):
    21- Don't forget your health when you are so involved in code! Good health = Good code! :3
    22- After I have done the entire assignment, I showed my code to a friend of mine that studied software engineering in Monash University and reminded me of using dictionaries. Would I have efficient code if I used them?! The good side of this is that I practiced using lists A LOT now.
"""
