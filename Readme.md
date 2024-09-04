# Neural Common Neighbour with Completion for Link Prediction using GraphSage

This project implements the Neural Common Neighbour with Completion (NCNC) algorithm for link prediction using GraphSage. The NCNC algorithm is based on the research paper titled [Neural Common Neighbour with Completion for Link Prediction], and it extends the GraphSage framework for more accurate link prediction in graph data.

## Files

- `NeighbourOverlap.py`: Python script implementing the neural common neighbour with completion for link prediction.
- `model.py`:  Contains the implementation of the GraphSage model.
- `utils.py`: Utility functions used in the project.
- `ogbdataset.py`: Helper functions for loading datasets from the Open Graph Benchmark (OGB).

## Datasets

The project supports three datasets for link prediction:

- Cora
- Citeseer
- Pubmed

## Running the Code

To reproduce the results on the datasets, run the following commands:


### Cora Dataset

!python NeighborOverlap.py --xdp 0.7 --tdp 0.3 --pt 0.75 --gnnedp 0.0 --preedp 0.4 --predp 0.05 --gnndp 0.05 --probscale 4.3 --proboffset 2.8 --alpha 1.0 --gnnlr 0.0043 --prelr 0.0024 --batch_size 1152 --ln --lnnn --predictor cn0 --dataset Cora --epochs 100 --runs 10 --model puregcn --hiddim 256 --mplayers 3 --testbs 8192 --maskinput --jk --use_xlin --tailact

### Citeseer Dataset

!python NeighborOverlap.py --xdp 0.7 --tdp 0.3 --pt 0.75 --gnnedp 0.0 --preedp 0.4 --predp 0.05 --gnndp 0.05 --probscale 4.3 --proboffset 2.8 --alpha 1.0 --gnnlr 0.0043 --prelr 0.0024 --batch_size 1152 --ln --lnnn --predictor cn0 --dataset Citeseer --epochs 100 --runs 10 --model puregcn --hiddim 256 --mplayers 3 --testbs 8192 --maskinput --jk --use_xlin --tailact


### Pubmed Dataset

!python NeighborOverlap.py --xdp 0.7 --tdp 0.3 --pt 0.75 --gnnedp 0.0 --preedp 0.4 --predp 0.05 --gnndp 0.05 --probscale 4.3 --proboffset 2.8 --alpha 1.0 --gnnlr 0.0043 --prelr 0.0024 --batch_size 1152 --ln --lnnn --predictor cn0 --dataset Pubmed --epochs 100 --runs 10 --model puregcn --hiddim 256 --mplayers 3 --testbs 8192 --maskinput --jk --use_xlin --tailact


Feel free to adjust the parameters as needed.


