# Common Errors

*First, delete any other code in your `main.py` file. Copy each code snippet below into `main.py` by clicking the copy icon in the top right of each code box. Then, hit `run` and see what errors occur. Fix the errors and press `run` again until you are error free. Click on the `👀 Answer` to compare your code to the correct code.*

👉 Can you figure out why this is crashing?

```python
import os, time
listOfEmail = []

def prettyPrint():
  os.system("clear") 
  print("listofEmail") 
  print()
  for index in len(listOfEmail): 
    print(f"{index}: {listOfEmail[Index]}") 
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
  elif menu == "3":
    prettyPrint() 
  time.sleep(1)
  os.system("clear")
  ```
<details> <summary> 👀 Answer </summary>

- The way we have constructed the `for` loop is strange. A `for` loop requires a `range` function. What we have right now (`for index in len(listOfEmail)`) literally means "for index in 1". That doesn't make sense? A loop of 1?
- We need to add the `range` function.

```python
 for index in range(len(listOfEmail)): 
    print(f"{index}: {listOfEmail[index]}") 
    counter += 1 
  time.sleep(1)
```

</details>