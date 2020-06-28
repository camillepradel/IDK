# IDK: Incomplete Data Knowledge base question answering
This repository contains dataset and code to reproduce experiments from the paper *Question Answering when Knowledge Bases are Incomplete* from Camille Pradel, Damien Sileo, Alvaro Rodrigo, Anselmo Peñas and Eneko Agirre.

The repository contains following files:
 - `idk_dataset.7z`: the dataset itself, containing:
   - `database`: a folder contaning for each database from the original Spider dataset a folder `[database_name]` with:
     - `[database_name].sqlite`: sqlite file of the altered database,
     - `alteration_report.json`: file stating the alterations which have been applied to the database (i.e. the list of deleted columns),
     - `original_schema.sql`: schema of the original database from the Spider dataset,
     - `schema.sql`: schema of the altered database,
   - `dev.json` and `train_spider.json`: files from original Spider dataset, with added field `answerability` stating answerability status for each question,
   - `tables.json` and `tables_empty.json`: parsed sql queries generated with `get_tables.py` script [from the Spider repository](https://github.com/taoyds/spider/blob/master/preprocess/get_tables.py),
 - `IDK_build_dataset.ipynb`: the notebook used to build the dataset, all set up tu be run in [Google colab](https://colab.research.google.com/github/camillepradel/idk/blob/master/IDK_build_dataset.ipynb).


## Citing
If you used our dataset, please kindly cite our paper

```
@inproceedings{pradel-2020-idk,
    title = "Question Answering when Knowledge Bases are Incomplete",
    author = "Pradel, Camille and Sileo, Damien and Rodrigo, Álvaro and Peñas, Anselmo and Agirre, Eneko",
    booktitle = "Proceedings of the Eleventh International Conference of the CLEF Association (CLEF 2020)",
    year = "2020"
}
```
as well as the original work
```
@inproceedings{Yu&al.18c,
  title     = {Spider: A Large-Scale Human-Labeled Dataset for Complex and Cross-Domain Semantic Parsing and Text-to-SQL Task},
  author    = {Tao Yu and Rui Zhang and Kai Yang and Michihiro Yasunaga and Dongxu Wang and Zifan Li and James Ma and Irene Li and Qingning Yao and Shanelle Roman and Zilin Zhang and Dragomir Radev}
  booktitle = "Proceedings of the 2018 Conference on Empirical Methods in Natural Language Processing",
  address   = "Brussels, Belgium",
  publisher = "Association for Computational Linguistics",
  year      = 2018
}
```

## License

Like the original Spider dataset, this work is licensed under a [Creative Commons Attribution 4.0 International
License][cc-by-sa].

[![CC BY 4.0][cc-by-image]][cc-by-sa]

[cc-by-sa]: https://creativecommons.org/licenses/by-sa/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by-sa/4.0/88x31.png