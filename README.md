# Game Demo
![Game Demo](demo_flappy.gif)

# Class Diagram
This is written with mermaid
```mermaid
classDiagram
    class Game{
        -BUTTON_GAP: int
        -best_scores: list
        -current_player_image
        -current_player_image_rect
        -current_player_index: int
        -game_over: bool
        -game_started: bool
        -gap: int
        -left_button: ImagesButton
        -obstacles: list
        -obstacles_distance: int
        -paused_button: ImagesButton
        -paused: bool
        -player
        -player_parameters: list
        -players: list
        -ranking_button: Button
        -restart_button: Button
        -resume_button: Button
        -right_button: ImagesButton
        -score: int
        -select_button: Button
        -setting_button: ImagesButton
        -start_button: Button

        +create_buttons()
        +display_scores_with_pandas()
        +display_setting_window(window)
        +draw()
        +draw_score()
        +end_game()
        +export_scores_to_csv(filename)
        +get_current_player()
        +get_current_player_description()
        +handle_events()
        +read_scores_from_csv(filename)
        +run()
        +show_character_select_window()
        +show_ranking()
        +show_getting_window()
        +start_game()
        +switch_to_next_character()
        +switch_to_previous_character()
        +update()
        +update_current_player_image()
    }
```
This is made by parsing main.py using pylint
![Class Diagram](classes_flappy.png)

# If you cannot enter docker
First open the terminal and type
```
$ sudo groupadd -f docker
```
Then type the following usermod command to add the active user to the **docker** group
```
$ sudo usermod -aG docker $USER
```
Apply the group changes to the current terminal session by typing
```
$ newgrp docker
```
Finally check if the **docker** group is in the list of user groups
```
$ groups
```

# How to run the game
First we have to enter docker
```
$ source Docker/docker_run.sh
```
After you enter docker
```
# python3 main.py
```
