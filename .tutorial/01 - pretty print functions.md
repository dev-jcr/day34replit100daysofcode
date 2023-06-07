# Pretty print Functions

Let's build a pretty `print` subroutine! So far all the subrouintes you have made have been *pretty* boring...just saying.

When we have a list of data, being able to print out that data in pretty ways is something we need to be able to do. So "pretty printing" is actually a thing. 

👉 I have created a program called "Spammer Inc." to spam emails (obviously this is not something you would actually do). If the user presses 1, they can add an email, and pressing 2 allows them to remove an email. (Hint: This should all look familiar so far).

```python
import os, time
listOfEmail = []

while True:
  print("SPAMMER Inc.")
  menu = input("1. Add email\n2: Remove email\n3. Show emails\n4. Get SPAMMING\n> ")
  if menu == "1":
    email = input("Email > ")
    listOfEmail.append(email)
  elif menu =="2":
    email = input ("Email > ")
    if email in listOfEmail:
      listOfEmail.remove(email)
  time.sleep(1)
  os.system("clear")
```

👉 What we have not done yet is `print` this out. Let's add a pretty `print` function. (Everything else in this code will stay the same).

```python
import os, time
listOfEmail = []

def prettyPrint():
  os.system("clear") # start by clearing the screen
  print("listofEmail") # print the title of my program
  print() # print a blank line
  for email in listOfEmail: # use for loop to access list
    print(email)
  time.sleep(1)

while True:
  print("SPAMMER Inc.")
  menu = input("1. Add email\n2: Remove email\n3. Show emails\n4. Get SPAMMING\n> ")
  if menu == "1":
    email = input("Email > ")
    listOfEmail.append(email)
  elif menu =="2":
    email = input ("Email > ")
    if email in listOfEmail:
      listOfEmail.remove(email)
    prettyPrint()  
  time.sleep(1)
  os.system("clear")
```

### Play around with your creation. Do you see what we did to make it 'pretty'?