# MuGNet-CMI

Circular RNAs (circRNAs) are non-coding RNA molecules that play a crucial role in regulating genes and contributing to disease progression. CircRNAs can function as sponges for miRNAs, thereby regulating gene expression and influencing disease outcomes. Identifying associations between circRNAs and miRNAs through computational methods enhances our understanding of complex disease mechanisms and offers a reliable tool for pre-selecting candidates for experimental validation. Existing models, however, are limited in their ability to capture either global or local node information, the prediction of circRNA and miRNA interactions is still challenging. In order to effectively deal with this problem, we propose a novel framework for predicting circRNA-miRNA interactions (CMIs), known as MuGNet-CMI, which leverages multi-head hybrid graph neural network and global high-order and local low-order information. The model employs the MetaPath2Vec algorithm to generate high-quality node embeddings within the circRNA-miRNA heterogeneous matrix. The multi-head dynamic attention mechanism, combined with GraphSAGE, is incorporated to efficiently capture both global high-order and local low-order node information. Additionally, we integrate neural aggregators into the multi-head dynamic attention mechanism to aggregate feature information from the captured nodes. Validation using three real datasets demonstrates that MuGNet-CMI delivers good performance in predicting circRNA-miRNA interactions, offering valuable insights to guide experimental research in gene regulation.

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
