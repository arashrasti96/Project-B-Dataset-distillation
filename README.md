# Project-B-Dataset_distillation

For all the notebook files, please first address the file to the correct directory by changing the first lines of the codes, and then run.

Task1 runs the approach in "Bo Zhao, Konda Reddy Mopuri, and Hakan Bilen. Dataset condensation with gradient matching.
ICLR, 1(2):3, 2021. https://arxiv.org/abs/2006.05929"

Task2 runs the approach in "Dataset distillation by matching training trajectories,. https://georgecazenavette.github.io/
mtt-distillation/"

Task2_DM runs the approach in "Bo Zhao and Hakan Bilen. Dataset condensation with distribution matching. arXiv preprint
arXiv:2110.04181, 2021. https://arxiv.org/abs/2110.04181"

# Dataset distillation for FL

In this scenario, we considered 10 clients where each has a local data set of size 1000. Each client will then condence their dataset and create 1 image per class. These data are gathered in "result_for_FL" file. Now, in an FL framework, each client will learn a model with a shared architecture using the condenced dataset, called local update. Next, they will send the weight of their model to the server. The server will aggregate the model using Federated Averaging (FedAvg) and then, distribute the aggregated global model to all clients. clients then try to do local updating again. The procudure repeats untill the shared model is converged.
