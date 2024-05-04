# Project-6-codeinplace2024karel
Checkerboard Karel (Python Programming)- Code In Place 2024 Stanford University

This Karel (Python Programming) Project provided by the popular coding program of Code in Place 2024 Stanford University-

* This python programming code works for karel different world

def main():
    run()
    end_position()
    
def run():
	put_beeper()
	complete_east_line()

# completeEastLine- front face line      
def complete_east_line():
	alternate_to_wall()
	turn_left()
	if front_is_clear():
		start_next_line()
		turn_left()
		complete_west_line()

# completeWeestLine- facing downwards second row
def complete_west_line():
	alternate_to_wall()
	turn_right()
	if front_is_clear():
		start_next_line()
		turn_right()
		complete_east_line()


# start next line
def start_next_line():
	if beepers_present():
		move()	
	else:
		move()
		put_beeper()

# alternate to wall
def alternate_to_wall():
	while front_is_clear():
		if beepers_present():
			move()
		else:
			move()
			put_beeper()

# command for turning right			
def turn_right():
    for i in range(3):
        turn_left()

# important code for karel to reach at it's final position after executing the task
def end_position():
    if right_is_blocked():
        turn_left()
    while front_is_clear():
        move()
    if right_is_clear():
       turn_left() 
    if front_is_blocked():
        turn_left()
    while front_is_clear():
        move()
    if front_is_blocked():
        turn_left()
![code in place 2024 checkerboard image](https://github.com/SHEETAL0812/Project-6-codeinplace2024karel/assets/128026212/f3657d80-1c71-497a-8824-c5e0339c9d1f)

