# Gym-docs

This repo contains the NEW website for [Gym](https://github.com/openai/gym). This site is currently in Beta and we are in the process of adding/editing information. 

Please see instructions below on how to contribute.

# Instructions for modifying environment docs

## Editing an environment page

If its an Atari environment, directly edit the md file in this repository. Otherwise, edit the docstring in the Gym Python file and then pip install your modified gym version and run `_scripts/gen_mds.py` in this repo. This will automatically generate a md documentation file for the environment.

## Adding a new environment

### Atari env

For Atari envs, add a md file into `pages/environments/atari` then complete the **other steps**

### Non-Atari env

Ensure the Python file corresponding to your environment has a properly formatted markdown docstring and is in gym (or your gym fork). Run `pip install -e .` inside the cloned gym repo. Then, run `_scripts/gen_mds.py`

### Other steps

- Add the corresponding gif into the `videos/` folder of the subfolder. Follow snake_case naming convention. Alternatively, run `_scripts/gen_gifs.py`.
- Edit `_data/pages` and add your new environment. Alternatively, `run _scripts/gen_menus` and replace the content in `_data/pages` within the #AUTOGENERATED comments with what is printed out.

# Editing other pages

Just PR to this repo
