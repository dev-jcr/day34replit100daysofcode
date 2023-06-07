# Creating a Numbered List

👉 I can also ensure my list prints as a numbered list. Let's make this happen by making these few changes below to our subroutine. This code snippet *only* shows the subroutine so we can focus on the changes there:


```python
def prettyPrint():
  os.system("clear") 
  print("listofEmail") 
  print()
  counter = 1 # add a counter
  for email in listOfEmail: 
    print(f"{counter}: {email}") # make this an f-string
    counter += 1 # adds a number with each new email
  time.sleep(1)

```

👉 We still need to call the subroutine. Let's edit our `while` loop a bit. 

```python
import os, time
listOfEmail = []

def prettyPrint():
  os.system("clear") 
  print("listofEmail") 
  print()
  counter = 1 
  for email in listOfEmail: 
    print(f"{counter}: {email}") 
    counter += 1 
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
  elif menu == "3": # we added this elif
    prettyPrint() # called our subroutine here
  time.sleep(1)
  os.system("clear")
  ```

  ### Can you add some color? Write your own pretty `print` function. Make it a numbered list, too.