# MuGNet-CMI


## Directory Structure

    code/
    ├── config.py         # Global configurations (command-line arguments, device settings, etc.)
    ├── main.py           # Main execution file (includes model training, testing, evaluation, etc.)
    ├── models/           # Contains model definitions
    │   ├── __init__.py   # (Can be empty, used to make the models folder a package)
    │   └── mugnet.py     # Includes definitions for FocalLoss, EarlyStopping, DMLP classifier, and MuGNET model
    └── utils/            # Contains various utility functions (data preprocessing, graph construction, random walk, feature generation, etc.)
        ├── __init__.py   # (Can be empty, used to make the utils folder a package)
        └── utils.py      # Specific implementations of various utility functions

    

## Running the Main Program

To run the program, simply execute the main.py file. This will initiate the full process of data loading, feature extraction, model training, and evaluation.

    python main.py

## Requirements

Ensure that the following Python packages are installed:

    pip install numpy keras scikit-learn joblib tqdm matplotlib

## Contributing

Contributions are welcome! If you find a bug or have a suggestion, please open an issue or submit a pull request.
