# Starcraft-2-Deep-Learning-Project
Using Deepmind's SC2 API, this project will attempt to program agents operating Starcraft to git gud and beat noobs in a completely recreational manner.

This project is built on 
- pysc2 (Deepmind) [https://github.com/deepmind/pysc2]

## File Locations
Map Locations
```shell
C:\Program Files (x86)\StarCraft II\Maps\Melee
```

pysc2 location
```shell
C:\Users\samte\AppData\Local\Programs\Python\Python36-32\Lib\site-packages\pysc2
```

## Useful Commands
Running pysc2 play file on the Simple64 map
```shell
python -m pysc2.bin.play --map Simple64
```


## Run an agent (Taken from Deepmind)

You can run an agent to test the environment. The UI shows you the actions of
the agent and is helpful for debugging and visualization purposes.

```shell
$ python -m pysc2.bin.agent --map Simple64
```

It runs a random agent by default, but you can specify others if you'd like,
including your own.

```shell
$ python -m pysc2.bin.agent --map CollectMineralShards --agent pysc2.agents.scripted_agent.CollectMineralShards
```

You can also run two agents against each other.

```shell
$ python -m pysc2.bin.agent --map Simple64 --agent2 pysc2.agents.random_agent.RandomAgent
```

To specify the agent's race, the opponent's difficulty, and more, you can pass
additional flags. Run with `--help` to see what you can change.

## Play the game as a human

There is a human agent interface which is mainly used for debugging, but it can
also be used to play the game. The UI is fairly simple and incomplete, but it's
enough to understand the basics of the game. Also, it runs on Linux.

```shell
$ python -m pysc2.bin.play --map Simple64
```

In the UI, hit `?` for a list of the hotkeys. The most basic ones are: `F4` to
quit, `F5` to restart, `F9` to save a replay, and `Pgup`/`Pgdn` to control the
speed of the game. Otherwise use the mouse for selection and keyboard for
commands listed on the left.

The left side is a basic rendering. The right side is the feature layers that
the agent receives, with some coloring to make it more useful to us. You can
enable or disable RGB or feature layer rendering and their resolutions with
command-line flags.

## Watch a replay

Running an agent and playing as a human save a replay by default. You can watch
that replay by running:

```shell
$ python -m pysc2.bin.play --replay <path-to-replay>
```

This works for any replay as long as the map can be found by the game.

The same controls work as for playing the game, so `F4` to exit, `pgup`/`pgdn`
to control the speed, etc.

You can save a video of the replay with the `--video` flag.

## List the maps

[Maps](docs/maps.md) need to be configured before they're known to the
environment. You can see the list of known maps by running:

```shell
$ python -m pysc2.bin.map_list
```

## Run the tests

If you want to submit a pull request, please make sure the tests pass on both
python 2 and 3.

```shell
$ python -m pysc2.bin.run_tests
```

Test
