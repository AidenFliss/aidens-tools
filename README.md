A basic library filled with some useful functions that are sometimes common use in python.

Install with:
```pip install aidens-basic-tools```

### Usage:
```python
import tools

#Flips a coin and print the result
print("Coin Flip is: " + str(tools.Random.coin_flip()))

tts = tools.TTS() # Init tts engine
tts.say("Hello there. Im Microsoft David!", True) # Says text and waits until the voice says it all

# Get if the current machine has internet
online = tools.get_internet_status(5) # Timeout of 5 seconds until its considered offline
if online:
  print("Online!")
else:
  print("Offline!")

def hello(hi):
  print(hi)

tools.Threading.delayed_thread(hello, 10, "This ran after 3 seconds without yielding!")
# This is right after the delay starts!

number = tools.Input.get_number_input_int("Enter an int: ", True)
print(number) # Get user input for an int, retry if input is invalid

float = tools.Input.get_number_input_float("Enter a float: ", True)
print(float) # Get user input for a float, retry if input is invalid

# Ask for item in list then check if its Dog or Cat
list = ["Cat", "Dog", "Person", "House"]
option = tools.Input.ask_for_item_in_list("Select an item: ", list, True)
if option == "Cat":
  print("Meow.")
elif option == "Dog":
  print("Woof!")

```
