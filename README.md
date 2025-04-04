# Code Red! On the Harmfulness of Applying Off-the-shelf Large Language Models to Programming Tasks

Replication Package for the FSE'25 Paper Titled: Code Red! On the Harmfulness of Applying Off-the-shelf Large Language Models to Programming Tasks

Additional visualisations of our data can be found in the [HuggingFace Space](AISE-TUDelft/Code-Red-Benchmark)

## Instructions
To run the project, follow these steps:

1. Create a virtual environment using conda by running: `conda create --name myenv python=3.10.8`. (Note that Python versions newer than 3.10 will not be supported by Autosklearn)
2. Activate the virtual environment by running: `conda activate myenv`.
3. Install the required Python packages by running: `pip install -r requirements.txt`.
4. Create 2 files with the respective API keys: `openai.key` and `openrouter.key` to run a single generation with the models we selected, you will need approximately €1 in OpenAI and €30 in Openrouter credits. 

The code is tested on an Ubuntu 20.04 LTS machine with 32GB of RAM and an Intel Core i9-12900HK processor.

## Results
The results of the experiments can be found in the `./results` folder, each file contains the results of a single model for a single generation for the entire dataset. The trained classifier can be found in the `./classification_models` folder, we only provide the best performing model to save space.

## Replication steps
1. **Classifier Training**: The `classifier.ipynb` notebook will run the experiments with the labelled data to create the classifiers. The classifiers are saved in the `/classification_models` folder. 
2. **Sample Generation**: `generation.ipynb` notebook will run generation with all the models. The results are saved in the `./results` 
3. **Sample Tagging**: `tagging.ipynb` will use the classifier from step 1 ot label the samples generated in the previous steps, the results will be saved in the `./results/tagged` folder. 
4. **Plotting**: `plots.ipynb` will take all the results and compile them into several figures used in the paper, each figure is saved in the `./plots` folder.

## Citation
Please cite our paper if you find our work useful:

```
misc{alkaswan2025codered,
      title={Code Red! On the Harmfulness of Applying Off-the-shelf Large Language Models to Programming Tasks}, 
      author={Ali Al-Kaswan and Sebastian Deatc and Begüm Koç and Arie van Deursen and Maliheh Izadi},
      year={2025},
      eprint={2504.01850},
      archivePrefix={arXiv},
      primaryClass={cs.SE},
      url={https://arxiv.org/abs/2504.01850}, 
}
```