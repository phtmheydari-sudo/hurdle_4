#  Hurdle 4 – Python Solution

This repository contains my solution for the Hurdle 4 challenge from Reeborg’s World.

---

## 🎬 Demo

This recording shows the robot navigating dynamically through the hurdles until reaching the goal.

![Demo](demo.gif)

---

## 📸 Screenshot

Final position of the robot after successfully completing the challenge.

![Screenshot](screenshot.png)


##  About the Challenge

The robot must reach the goal while navigating hurdles of different heights and positions.

The solution must:
- Adapt dynamically
- Detect open paths
- Continue until reaching the goal

---

##  Strategy

The robot follows a right-hand rule:

1. If the right side is clear → Turn right and move
2. Else if the front is clear → Move forward
3. Otherwise → Turn left

---

##  Code

```python
def turn_right():
    turn_left()
    turn_left()
    turn_left()

while not at_goal():
    if right_is_clear():
        turn_right()
        move()
    elif front_is_clear():
        move()
    else:
        turn_left()
