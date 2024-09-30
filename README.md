# Dosg Bread Classifier

### [Dogs Dataset](https://www.kaggle.com/datasets/khushikhushikhushi/dog-breed-image-dataset)
In Order to run program successfully, modification `.env` file
###### step 1: download API key from kaggle
![kaggle key](./assets/kaggle_key.png)
- create new key
- paste it on `.env`file

###### step 2: modify .env file
```
username=
key=
```


### Project Folder Structure
```sh.
$ tree --dirsfirst -L 2 -a -I .git .
├── configs
│   ├── callbacks
│   ├── data
│   ├── experiment
│   ├── hydra
│   ├── logger
│   ├── model
│   ├── paths
│   ├── trainer
│   ├── train_old.yaml
│   └── train.yaml
├── data
├── Dockerfile
├── .env
├── pyproject.toml
├── README.md
├── src
│   ├── datamodules
│   ├── infer.py
│   ├── models
│   ├── train.py
│   └── utils
└── tests
    ├── conftest.py
    ├── datamodules
    ├── models
    └── test_train.py

```



```sh
python src/train.py data.batch_size:64 model.pretrained=false trainer.max_epochs=10
```