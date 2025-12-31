## gofish (a CS2 selfbot)

gofish is a somewhat simple python script to generate responses to commands by sending a keystroke which executes a config file ingame.

## Features
- `!fish`
  - Fishing minigame!

## Game Setup
1. Add this to your Steam Launch Options for CS2: `+exec autoexec.cfg -condebug -con_clearlog`
2. Add the following to your [autoexec.cfg](https://www.prosettings.com/csgo-config-autoexec-guide/). Or you can add it like I have it in [my autoexec.cfg](https://github.com/Trevo525/cs2-autoexec).
```
bind "[" "say !fish"
bind "]" "exec selfbot.cfg"
log_flags InputService +donotecho // absolutely NEEDED due to CS2 having really fucking annoying limitations and the only way for me to send console commands is with "exec"
log_flags Prediction +donotecho
log_flags "CL CommandQueue" +donotecho

echo "selfbot initialized"
```

## Requirements

- [Python 3.11](https://www.python.org/downloads/release/python-3119/) (only version I tested)
- [Poetry](https://python-poetry.org/)

## Installing

1. Install [Python 3.11](https://www.python.org/downloads/release/python-3119/)
2. Install [Poetry](https://python-poetry.org/)
3. Clone the repo into a folder on your computer.
4. Run `cd galls` inside of a terminal window.
5. Run `poetry install` inside of a terminal window to install dependencies.
6. Make a copy of `.env.example` and name it `.env`, edit it to contain the correct environment variables needed for the script to work.
7. Run `poetry run python main.py` inside of the project directory.

## Authors

  - [Pandaptable](https://github.com/Pandaptable) 
  - [DeaFPS](https://twitter.com/deafps_) for letting me yoink her code and convert it to python... also making the fish database because [fishbase](http://www.fishbase.us/) is way too big.. ly loser <3
