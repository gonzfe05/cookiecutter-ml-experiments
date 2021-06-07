# Project structure
Simple template for ML experiments.  
You have to define project and experiment names in the `cookiecutter.json` file.  
Includes container for developing inside [vscode remote containers](https://code.visualstudio.com/docs/remote/containers).  

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

### Usage
Install with `pip install cookiecutter`.  
To create new directory from template, just run `cookiecutter $template_path`.  
Anything else check the [official docs](https://cookiecutter.readthedocs.io/en/1.7.2/first_steps.html)

Inspired from [Martin Thome post](https://martin-thoma.com/ml-best-practice/)
