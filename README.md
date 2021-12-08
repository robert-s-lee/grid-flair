
Grid.ai demo of [Flair](https://github.com/flairNLP/flair).  Flair is A very simple framework for state-of-the-art NLP. Developed by [Humboldt University of Berlin](https://www.informatik.hu-berlin.de/en/forschung-en/gebiete/ml-en/) and friends. 

Please have Grid.ai prerequisites:
- login into [Grid.ai](#start-a-gridai-g4dnxlarge--1-x-t4-session)
- start a Session with GPU instance
- [Start Jupyter Notebook](#start-a-jupyter-notebook) 

To run `bash` commands in this example, one of the following methods can be used: 
- From Grid.ai Jupyter Notebook: `File` -> `New` -> `Terminal`
- From Terminal: `grid session ssh`
- From VS Code: `Command P` -> `Remote SSH: Connect to Host`
- 
# Setup Grid.ai Session 

- setup Conda environment
```bash
conda create --yes --name flair python=3.8
conda activate flair 
pip install ipykernel 
python -m ipykernel install --user --name=flair 
ipython profile create
```
- setup Grid.ai specific libraries
```
pip install lightning-grid
```
- setup Flair specific libraries
```
pip install flair
```
- clone this repo
```
git clone https://github.com/robert-s-lee/grid-flair
cd grid-flair
pip install -r requirements.txt
```

## Run Flair [example usage](https://github.com/flairNLP/flair#example-usage)

```
% python run.py

2021-12-08 14:24:42,009 --------------------------------------------------------------------------------
2021-12-08 14:24:42,010 The model key 'ner' now maps to 'https://huggingface.co/flair/ner-english' on the HuggingFace ModelHub
2021-12-08 14:24:42,010  - The most current version of the model is automatically downloaded from there.
2021-12-08 14:24:42,010  - (you can alternatively manually download the original model at https://nlp.informatik.hu-berlin.de/resources/models/ner/en-ner-conll03-v0.4.pt)
2021-12-08 14:24:42,010 --------------------------------------------------------------------------------
Downloading: 100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 432M/432M [00:32<00:00, 13.4MB/s]
2021-12-08 14:25:14,835 loading file /Users/robertlee/.flair/models/ner-english/4f4cdab26f24cb98b732b389e6cebc646c36f54cfd6e0b7d3b90b25656e4262f.8baa8ae8795f4df80b28e7f7b61d788ecbb057d1dc85aacb316f1bd02837a4a4
Sentence: "I love Berlin ."   [− Tokens: 4  − Token-Labels: "I love Berlin <S-LOC> ."]
The following NER tags are found:
Span [3]: "Berlin"   [− Labels: LOC (0.999)]
```

# Optional

- TODO: fix up the example 

```
pip install pytest
git clone https://github.com/flairNLP/flair
cd flair
```

