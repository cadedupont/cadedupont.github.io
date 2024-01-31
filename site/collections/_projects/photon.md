---
title: Photon
subtitle: An update to the classic laser tag game, Photon
image: /assets/img/projects/photon.jpg
priority: 1
---

# Details
We will be recreating the control console for the popular Photon laser tag game. The console controls the major functionality of the game.

# Prerequisites
- Python 3
- Tkinter
- Supabase account and authentication credentials (visit the [supabase-py documentation](https://supabase.com/docs/reference/python/introduction) for more information)
   - You should have a `.env` file in the root directory of the project with the following variables:
      - `SUPABASE_URL` - the URL of your Supabase project
      - `SUPABASE_KEY` - the public key of your Supabase project
   - Make sure you have a table named `users` with an `id` column of type `int8` and a `username` column of type `text`

# Major Components
1. Player entry console with Supabase connection for entering and storing user information
2. UDP connection for sending and receiving data from the Photon laser tag units
3. GUI for displaying actions from units along with updating player and team scores

# Run Instructions
Open a terminal window and clone this repository to your local machine:

`git clone https://github.com/cadedupont/photon.git`

Open 2 terminal windows and navigate to the root directory of the cloned repository in both.
Note that `python` and `pip` are interchangable with `python3` and `pip3` - whichever command your machine utilizes for Python 3.

## Running the traffic generator
Provided in the `src` directory is a file named `traffic_generator.py`. This file will generate UDP traffic to simulate the Photon laser tag units. In one of your terminal windows, run the following to start the traffic generator:

`python src/traffic_generator.py`

The program will prompt you to enter 2 equipment IDs for each team. We recommend using 10 and 20 for the green team and 30 and 40 for the red team.

## Running the main Photon program
A Makefile is provided to simplify running the main program. In your second terminal window, run the following:

Install the project's required dependencies:

`make init` or `pip install -r requirements.txt`

Run the main program:

`make run` or `python src/main.py`

Clean up the project's generated files:

`make clean` or `rm -rf src/__pycache__`

Running `make` without any arguments will run `init`, `run`, and `clean` in that order. Or, running `make reset` will run `clean` and `init`.

The player entry console will require using the `<tab>` key to switch between each field. When you've completed registering players for one team, use the mouse to select the other team's first equipment ID field and continue registering players. Click either the `Continue` button or press `<F5>` to finalize player registration and continue to the countdown screen. Press `<F12>` while still in the player entry console to clear all player entries.

Make sure that the equipment IDs you entered in the traffic generator match the ones you entered in the player entry console.

# Screenshots:
<p align="center">
   <img width=800px src="https://github.com/cadedupont/photon/assets/98860495/84c119e4-2a8c-46d4-8211-1de6e134f328"><br>
   <img width=800px src="https://github.com/cadedupont/photon/assets/98860495/463e9643-5aac-4f93-a45a-d17e6f48d3ee"><br>
   <img width=800px src="https://github.com/cadedupont/photon/assets/98860495/87e2d5c5-1083-43fe-8a02-ea62434ecdcf"><br>
</p>