# Neurotech Club GitHub - TODO - Fill this out

Foobar is a Python library for dealing with word pluralization.

## Installation

Create a conda environment

TODO: create a neurotech_club_env.yml with necessary packages and add to this GitHub!! THE FOLLOWING WILL NOT DO ANYTHING YET! 
```bash
conda env create -f neurotech_club_env.yml
```

## Usage
Please set all hyperparameters for the model in config.json. When creating new model types and modifying old ones,
please ensure that all hyperparameters of interest can be adjusted in config.json so that there is only ONE place 
to do so. This may be a bit annoying, but the config.json files are saved in results/saved_models/configs so that we
know exactly how we built a specific model.
```json
{
    "settings": {
        "root_path": "Directory in which main.py is stored",
        "data_path": "Directory in which data is stored (file names must follow Neurotech Club's conventions)"
    },

    "data": {
        "subjects": ["array", "of", "subjects"],
        "electrodes": ["array", "of", "electrodes"],
        "waves": ["array", "of", "waves"]
    },

    "model": {
        "model_type": "name_of_model_to_use_see_below",
        "baby_binary": {
            "num_hidden_layer_nodes": <int_num_nodes>
        },
        "dnn_binary": {
            "hidden_layers": [<int_num_nodes_layer_1>, <int_num_nodes_layer_2>, ...]
        }
    },

    "train": {
        "epochs": <int_num_epochs>,
        "learning_rate": <int_learning_rate>
    }
}
```
```bash
python main.py
```