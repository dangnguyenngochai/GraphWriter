# Update
- Data formatted and processed in `preprocessed.[train|val|test].tsv` include the following fields:
  - "title" of the papper
  - "entities" extracted
  - "entities type" following the order of "entities"
  - "text" is the equivalent text with placeholders of entities
  - the last part is the appearance order of the "entities", although the authors stated in [this](https://github.com/rikdz/GraphWriter/issues/4) that the field is not used

- `lastGraph2_sents.tsv` and order `preprocess*` seem to be the same, but only the later is used in code

# Text Generation from Knowledge Graphs with Graph Transformers

This repository contains the source code of our paper, [Text Generation from Knowledge Graphs with Graph Transformers](https://arxiv.org/abs/1904.02342), which is accepted for publication at [NAACL 2019](http://naacl2019.org/).

# Instructions

Training:
```
python3.6 train.py -save <DIR>
```
Use ``--help`` for a list of all training options.

To generate, use 
```
python3.6 generator.py -save <SAVED MODEL>
``` 
with the appropriate model flags used to train the model

To evaluate, run
```
python3.6 eval.py <GENERATED TEXTS> <GOLD TARGETS>
```


# AGENDA Dataset

The AGENDA dataset is available in a user-friendly json format in /data/unprocessed.tar.gz
Preprocessed data is also available in /data.


## Citation
If this work is useful in your research, please cite our paper.
```
@inproceedings{koncel2019text,
  title={{T}ext {G}eneration from {K}nowledge {G}raphs with {G}raph {T}ransformers},
  author={Rik Koncel-Kedziorski, Dhanush Bekal, Yi Luan, Mirella Lapata, and Hannaneh Hajishirzi},
  booktitle={NAACL},
  year={2019}
}
```

