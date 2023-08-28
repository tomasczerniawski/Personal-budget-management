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
