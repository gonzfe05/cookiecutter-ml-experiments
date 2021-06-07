# Project structure
Simple template for ML experiments.
You have to define project and experiment names in the `cookiecutter.json` file.

```bash
.
├── artifacts
│   ├── train : Logfiles
|   |   └── models : trained models
│   └── test  : Logfiles
├── datasets : Data loading scripts
├── experiments : YAML defining the experiments parameters
├── models : YAML defining models
├── optimizers : YAML defining optimizers
└── train : Script to run the training
```

All hyperparameters, including the complete model, should be set in the configuration.

Inspired from [Martin Thome post](https://martin-thoma.com/ml-best-practice/)