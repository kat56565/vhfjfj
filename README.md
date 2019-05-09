# Program ID: Trying to get out of a scary house
# Author: Kathryn Chen
# Program Description: using codes to figure out how to get out of a house with enemy

playagain = "yes"

intro = """You have been brought to a mysterious house by an
        armed black suited man. You have no choice but to go
        in. Before you opened the door the man said, 'It's just
        a test, don't be scared. Find the key, and get out.
        That's all. Have fun.' You stepped in, and he stopped you
        again. 'Oh! I forgot, there's a man waiting for you, he's
        afraid of hot water *cough cough*, you have been warned.'
        Now you are more than terrified. Good Luck."""
print(intro)

def living_room():
    definition = """You are currently in the Living Room of the house.
    It is very dark, there's slight stray of light coming
    from the kitchen on the east. To the south is some stairs
    leading upstairs. You can see there is a red sofa and a
    table lamp."""

    print(definition)

    user_input = input()
    if user_input == "turn on lamp":
        print("""You have turned on the lights, now you can see
        things better now, you noticed a secret door!""")
        user_input = input()
    if user_input == "east":
        kitchen()
    if user_input == "south":
        stairs()
    if user_input == "go to secret door":
        secret_hallway()

def kitchen():
    definition = """You have arrived in the kitchen, there is a big
     black fur rug in the middle when you walked over it you noticed
     something under it. On the counter there is a cup of water. To
     the east is the bathroom."""

    print(definition)

    user_input = input()
    if user_input == "west":
        living_room()
    if user_input == "east":
        bathroom()
    if user_input == "lift rug":
        user_input2 = input("Congrats, you found a Key, but where is it for?")
        if user_input2 == "put in inventory":
            print("you now have a key")
    if user_input == "drink water":
        user_input2 = input("Water drank, do you want to put cup in inventory?")
        if user_input2 == "yes":
            print("You put cup into inventory")

def bathroom():
    definition = """ You're in the bathroom. There is a mirror, sink,
    shower, and a toilet. A normal bathroom. """

    print(definition)

    user_input = input()
    if user_input == "west":
        kitchen()
    if user_input == "flush toilet":
        print("You were able to flush the toilet, the water works.")
    if user_input == "turn sink water on":
        print("You were able to turn on water, it works *cough cough* ")
    if user_input == "use cup from inventory":
        print("You took the cup out")
    if user_input == "get hot water with cup":
        user_input2 = input("You now have a cup of hot water.")
        if user_input2 == "yes":
            print("You put cup of hot water into inventory")

def stairs():
    definition = """ You are at the front of the stairs. You hear movement upstairs."""

    print(definition)

    user_input = input()
    if user_input == "go up":
        hallway()

def hallway():
    definition = """ You are in the hallway of the second floor
    of this house. There is a Master's (south), Kid'd Room (east),
    and a broom sitting outside of the master's. Maybe it will
    come in handy. To go back down to living room go north."""

    print(definition)

    user_input = input()
    if user_input == "north":
        living_room()
    if user_input == "south":
        masters()
    if user_input == "east":
        kid_room()
    if user_input == "pick up broom":
        user_input2 = input("You have picked up the broom")
        if user_input2 == "put in inventory":
            print("The broom is in inventory")

def masters():
    definition = """ There's a nice elegant bed in the middle
    and in the corner of your eye you see a person with a key
    hanging from his neck. He looks very mean, he might be the
    guy the person warned you about."""

    print(definition)

    user_input = input()
    if user_input == "use broom to hit him ":
        print("that was a smart move, he go hurt")
        user_input2 = input("Do you have cup of hot water in your inventory")
        if user_input2 == "yes":
            print("""You took the hot cup of water and slashed it
            in his face. He cant see anything anymore. You quickly
            took the key from his neck.""")
    if user_input == "use hot water":
        print("")

def kid_room():
    definition = """ """

def secret_hallway():
    definition = """ """


while playagain == "yes":
    living_room()
    input("do you want to play again?")
