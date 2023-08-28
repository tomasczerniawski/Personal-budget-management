# Personal Budget Management

The project aims to help users manage their personal budget. The project will include features such as adding, editing, and deleting expenses and income, allowing users to track their budget and generate reports.

## Structure Description

### BinaryTreeNode<T>

Class representing a node in a binary tree. It has the following fields:

- `data` (type `T`): Stores data representing income or expense.
- `left` (type `BinaryTreeNode*`): Pointer to the left subtree.
- `right` (type `BinaryTreeNode*`): Pointer to the right subtree.

### BinaryTree<T>

Class representing a binary tree. It has the following fields:

- `root` (type `BinaryTreeNode<T>*`): Pointer to the root of the tree.

### FinanceManager

Class managing finances. It has the following fields:

- `CURRENT_USER_ID` (type `const int`): Identifier of the current user.
- `incomesBinaryTree` (type `BinaryTree<Income>`): Binary tree storing incomes.
- `expensesBinaryTree` (type `BinaryTree<Expense>`): Binary tree storing expenses.
- `incomesFile` (type `IncomesFile`): Object handling the income data file.
- `expensesFile` (type `ExpensesFile`): Object handling the expense data file.
- `date` (type `Date`): Object representing a date.
- `totalIncome` (type `float`): Total income within a specified period.
- `totalExpense` (type `float`): Total expenses within a specified period.
- Other fields containing methods and functions.

## Parameter Types in Structures

The following parameter types are used in the above structures:

- `T`: This is a template parameter representing the type of data stored in the binary tree. In the case of `incomesBinaryTree`, it's the type `Income`, and in the case of `expensesBinaryTree`, it's the type `Expense`.
- `Income`: Class representing income.
- `Expense`: Class representing expense.
- `IncomesFile`: Class handling the income data file.
- `ExpensesFile`: Class handling the expense data file.
- `Date`: Class representing a date.

# Programming Language: C++
I chose the C++ language for this project for several reasons:
- Object-Oriented: C++ is an object-oriented programming language, enabling structured and modular application design. We can use classes and objects to logically group related functions and data.
- Libraries and Tools: It offers a wide range of libraries and tools that can be useful for creating a finance management project. For instance, we can utilize libraries for file handling, data structures, and mathematical calculations.
- Considering other programming languages, I have worked with C++ the most.

Taking these factors into account, C++ is a suitable choice for a finance management project.

# Structure Description (Directory Organization) and File Names

The Financial project follows the following directory organization structure and file names:

## Main and Only Directory

- `src/`: Directory containing project source files.
## Directory src/

:page_facing_up: `AdjuvantMethods.cpp:` Source file containing auxiliary methods.

:page_facing_up:  `AdjuvantMethods.h:` Header file containing declarations of auxiliary methods.
  
:scroll:  **Budget.cpp:** Source file containing the implementation of the Budget class.

:scroll: **Budget.h:** Header file containing the declaration of the Budget class.

:page_facing_up: `Date.cpp:` Source file containing the implementation of the Date class.
  
:page_facing_up: `Date.h:` Header file containing the declaration of the Date class.

:scroll: **Expense.cpp:** Source file containing the implementation of the Expense class.
  
:scroll: **Expense.h:** Header file containing the declaration of the Expense class.

:page_facing_up: `ExpensesFile.cpp:` Source file containing the implementation of the ExpensesFile class.
  
:page_facing_up: `ExpensesFile.h:` Header file containing the declaration of the ExpensesFile class.

:scroll: **Finance.cpp:** Source file containing the implementation of the Finance class.
  
:scroll: **Finance.h:** Header file containing the declaration of the Finance class.

:page_facing_up: `FinanceManager.cpp:` Source file containing the implementation of the FinanceManager class.
  
:page_facing_up: `FinanceManager.h:` Header file containing the declaration of the FinanceManager class.

:scroll:  **Income.cpp:** Source file containing the implementation of the Income class.
  
:scroll:  **Income.h:** Header file containing the declaration of the Income class.

:page_facing_up:  `IncomesFile.cpp:` Source file containing the implementation of the IncomesFile class.
  
:page_facing_up:  `IncomesFile.h:` Header file containing the declaration of the IncomesFile class.

:scroll:  **Markup.cpp:** Source file containing the implementation of the Markup class.
  
:scroll:  **Markup.h:** Header file containing the declaration of the Markup class.

:page_facing_up:  `User.cpp:` Source file containing the implementation of the User class.
  
:page_facing_up:  `User.h:` Header file containing the declaration of the User class.

:scroll: **UserManager.cpp:** Source file containing the implementation of the UserManager class.
  
:scroll: **UserManager.h:** Header file containing the declaration of the UserManager class.

:page_facing_up:  `UsersFile.cpp:` Source file containing the implementation of the UsersFile class.
  
:page_facing_up:  `UsersFile.h:` Header file containing the declaration of the UsersFile class.

:scroll: **XmlFile.cpp:** Source file containing the implementation of the XmlFile class.
  
:scroll: **XmlFile.h:** Header file containing the declaration of the XmlFile class.

:page_facing_up:  `main.cpp:` Source file containing the main() function.


  
# Algorithms and Data Structures Used in the Project

The file BinaryTree.h implements the binary tree data structure (Binary Tree) and the corresponding algorithms operating on this structure.

## Data Structure

### BinaryTreeNode
The class `BinaryTreeNode` represents a node in a binary tree. It has three fields: 
  
- `data:` storing the value of the node
- `left` and `right`, pointing to the left and right subtree.

### BinaryTree
The class `BinaryTree` represents a binary tree. It has a field
- `root:` pointing to the root of the tree. The class provides methods for inserting nodes, performing in-order traversal, and searching nodes based on a given keyword.

## Algorithms

### insertRecursive
- The `insertRecursive` method is a recursive algorithm for inserting nodes into a binary tree. It searches for the appropriate place in the tree to insert a new node based on the key value. If the node is smaller than the current node, it's inserted into the left subtree; otherwise, it's inserted into the right subtree.
  
  ![image](https://www.codesdope.com/staticroot/images/ds/bst9.gif)
  
  **In my code:**
 - Objects are compared based on the value of their price (Amount). If the Amount of a given object is smaller than the Amount of the current node, the object is inserted into the left subtree. Otherwise, if the Amount is greater than or equal to the Amount of the current node, the object is inserted into the right subtree. This way, the binary tree is constructed in a manner that the Amount values are ordered in ascending order within the tree.


### inOrderTraversalRecursive
- The `inOrderTraversalRecursive` method is a recursive algorithm for performing an in-order traversal of a binary tree. It traverses the tree in ascending order, first visiting the left subtree, then the current node, and finally the right subtree. In this case, the value describing the node is printed to the standard output.
  
  ![image](https://lh3.googleusercontent.com/QRTgAbTK-54jPLU87RN4OAXWlBu1WR36LyaANNQ_Pg0N2gKmM0k_30h5S68Dwm_2qledVGQd5Byltj16KO3J5ufZs1ipixS4DKpHTRITXDiHajiLXEjf_sY7Id7e8G7r4mhBbANn)
  
### searchRecursive
- The `searchRecursive` method is a recursive algorithm for searching nodes in a binary tree based on a given keyword. It searches the tree by comparing node descriptions with the provided keyword. If the node is found, it's returned. Otherwise, the algorithm recursively searches the left and right subtrees.

  ![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/83f2302b-2e6e-40b2-b90f-e401ae3ec8d0)

  **In my code:
  
- The "search" method takes a parameter "keyword," which represents the description we are looking for in the tree. The method calls the "searchRecursive" function, passing it the tree root ("root") and the desired "keyword." The "searchRecursive" function starts by checking if the current node is empty or if its description matches the searched "keyword." If so, it returns that node.

- If the description of the current node doesn't match the searched "keyword," the function recursively calls itself for the left and right subtrees. If a node is found in the left subtree, it returns that node. Otherwise, it calls itself for the right subtree.

- If no node with a matching "keyword" description is found, the "search" function returns nullptr.

  
# In the FinanceManager.cpp file
  
## Algorithms
  
### Bubble Sort
- Bubble Sort is a simple sorting algorithm that compares adjacent elements and swaps them if they are in the wrong order. The algorithm performs these operations in a loop, iterating through the list multiple times until the list is sorted.

  ![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/beff2f5c-7fda-4af1-b899-b777127afd25)

  In this code, Bubble Sort is used to sort data in a binary tree. The algorithm compares and swaps nodes based on their income values.
  
# Functions:
  
### This function presents the program's login menu
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/281e3ade-4f49-476a-94ea-18deeb2ceb9d)

- `Main Menu:` The function displays the main program menu, where the user can choose one of three options:

- Sign up: This option allows the user to register a new account. Upon choosing this option, the user is prompted to enter their registration details, such as username and password. Then, these details are processed and saved in an XML file where a unique identification number (UserId) is assigned, enabling the user to use the program.

- Sign in: This option allows the user to log in to an existing account. Upon choosing this option, the user is prompted to enter their username and password for authentication. If the login data is correct, the user gains access to the full program functionality.

- Exit: This option allows the user to exit the program. Upon choosing this option, the program is closed and terminated.
  
### Main menu of the Personal Budget Management project
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/2ed0f216-047a-4f2b-a09d-96b7e755ad7d)
  
## Function Add Income (Choice No. 1)
  
### Add income
  
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/c9a0d5d3-443a-4722-842b-fd823d8b4c6f)

  - The "Add income" option allows the user to add new income to the system. Upon selecting this option, the user is guided through the process of entering income-related data, such as date, item, and amount, which are automatically assigned. Each income also receives a user identifier and income identifier. Then, the function calls the "addIncomeToXmlFile" function to add the income to the XML file. If the addition is successful, a confirmation message is displayed. After completion, the user is asked to press any key to continue.
  
## Function Add Expense (Choice No. 2)

### Add expense
  
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/be705b86-d220-4382-8f20-1caf45bc4c22)

  - The "Add expense" option allows the user to add new expense to the system and works in the same way as "Add income."
  
## Function View Current Month's Balance (Choice No. 3)
  
### View current month's balance
  
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/c7e3aa5a-61fb-4698-bad5-1a010649c8bd)

 - The "viewCurrentMonthBalance" function is used to display the balance of the current month. It first calculates the minimum and maximum dates for the current month based on the current system date. Information about current month's incomes and expenses are displayed, along with a summary.

- The function calls the "viewSelectedIncomes" function to display the incomes for the specified date range (from minDate to maxDate) using a binary tree structure. Then, the "viewSelectedExpenses" function is called to display the expenses of the current month.

- The "viewSelectedIncomes" function traverses the binary income tree in an inorder fashion using a stack. For each node, it checks if the income date falls within the specified date range (minDate to maxDate). If so, income details (e.g., name and amount) are displayed on the console.

- The function concludes when it has traversed all income and expense nodes in the same manner or when the stack is empty.
  
## Function View Balance of the Selected Period (Choice No. 4)
  
### View balance of the selected period
  
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/efc3be6e-9470-413b-959d-a6aa9c95cc29)

- The "viewBalanceOfSelectedPeriod" function is used to display the balance for a selected period. The user is prompted to provide a start and end date for the period they want to view. The function then calculates the minimum and maximum dates for that period.
- It works in the same way as the previous function, but here the user specifies the period they want to analyze.
  
## Function View All Incomes/Expenses (Choice No. 5/6)
  
### View all incomes/expenses:
  
  - I'm combining these two options since they work similarly.
  
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/26c3e90b-6f09-46fd-bbdd-0a5785a55866)

- The "viewAllIncomes" function is used to display all incomes. It starts by calling the "viewIncome" function, passing it the binary income tree root "incomesBinaryTree."

- The "copyBinaryTree" function copies a binary tree passed as the "node" argument. A new node with the same value is created, and then left and right subtrees are recursively copied. It's used to avoid modifying the original tree; a copy is created on which these operations are performed.

- The "deleteBinaryTree" function is used to delete a binary tree. It recursively deletes left and right subtrees, and then the node itself.

- The "viewIncome" function initializes the income display. It begins by making a copy of the original income tree using the "copyBinaryTree" function. Then, it presents the user with sorting options for incomes, such as sorting by date (newest or oldest) or sorting by amount (cheapest or most expensive). The user's choice is stored in the "choice" variable.

- Depending on the user's choice, incomes are displayed in the specified sorting order. Functions like "viewIncomeByDateNewest," "viewIncomeByDateOldest," "sortIncomesByAmount," "displayIncomesByAmount," and "viewIncomeByPriceMostExpensive" are called based on the user's selection.

- "viewIncomeByDateNewest" and "viewIncomeByDateOldest" functions display incomes sorted by date, with the newest or oldest displayed first. They use a stack to traverse the binary income tree in reverse order (right, root, left), storing the sorted incomes in the "sortedIncomes" container.

- The "countNodes" function counts the number of nodes in a binary tree. It recursively calculates the number of nodes in the left and right subtrees, then adds one for the current node.

- The "sortIncomesByAmount" function sorts incomes by amount using the bubble sort algorithm. It first counts the number of nodes in the subtree, then compares adjacent nodes' amounts and swaps them if one's amount is greater than the other's. This procedure is repeated for all nodes.

- The "displayIncomesByAmount" function displays incomes by amount using an inorder traversal (left, root, right). It's recursively called for the left subtree, the current income is displayed, and then it's recursively called for the right subtree.  

## Function Search in Budget (Choice No. 7)
  
### Search in budget
  
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/ef741b7b-7b99-476e-a517-2c7a573fa1e1)
  
 - The "searchIncomesAndExpenses," "searchIncomeByItemRecursive," and "searchExpenseByItemRecursive" functions are used for searching incomes and expenses based on a provided keyword.

- The "searchIncomesAndExpenses" function initiates the search process. It calls two other recursive functions: "searchIncomeByItemRecursive" and "searchExpenseByItemRecursive."

- The "searchIncomeByItemRecursive" and "searchExpenseByItemRecursive" functions recursively search the income and expense binary trees for nodes with an "item" element that matches the provided keyword. If such nodes are found, the "displayIncome" or "displayExpense" function is called to display the details of the found income or expense. The "resultsFound" parameter is used to track if any results were found.

## Function Generate Report (Choice No. 8)
  
### Generate report
  
![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/a3d1af62-022a-4c03-9e76-b3d50177422c)

 - The "generateMonthlyIncomeChart," "countMonthlyIncomes," and "countMonthlyExpenses" functions are used to generate a monthly budget report.

- The "generateMonthlyIncomeChart" function initiates the report generation process. It prompts the user to provide a start and end date for the period they want to view. Then, it calls other functions like "viewSelectedIncomes," "viewSelectedExpenses," "calculateTotalIncome," and "calculateTotalExpense" to display selected incomes and expenses and calculate the total income and expense for the specified period.

- The function then generates a chart of monthly budget in the specified period. It creates a vector called "monthlyIncomes" to store income amounts for each month. It iterates over income nodes and accumulates income amounts for each month. The chart is presented using "#" and "---" symbols based on the income amounts.

- Finally, the function displays a summary of the selected period, including the total income, total expense, and monthly budget.

- The "countMonthlyIncomes" and "countMonthlyExpenses" functions are helper functions that recursively traverse the binary income and expense trees, calculating income and expense sums for each month in the specified period. The found amounts are stored in "monthlyIncomes" and "monthlyExpenses" vectors.

## Function Generate Random Budget (Choice No. 9)
  
### Generate random budget
  
  ![image](https://github.com/tomasczerniawski/Project-Personal-budget-management/assets/115027239/c598b766-4fa5-425b-ae8f-41006c92375c)
  
- The user is prompted to provide a start and end date for the period, minimum and maximum amount, and the number of generated expenses and incomes.
Random amount within the specified range is generated using the "rand()" function and mathematical operations.

- Generating a random date within the specified range is based on minimum and maximum year, month, and day values, using "rand()" function to generate random values for these date components.
  
- Additionally, the function uses binary trees ("incomesBinaryTree" and "expensesBinaryTree") to store generated incomes and expenses. When generating an income, an "Income" class object is created and added to "incomesBinaryTree." For expenses, an "Expense" class object is created and added to "expensesBinaryTree."

