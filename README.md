# RoCar
This repository is the basic schemas, antonomasias, and the knowledge of relationships referred to in **[RoCar: A Relationship Network-based Evaluation Method to Large Language Models](https://arxiv.org/abs/2307.15997).**

## Files
- `antonomasia.csv` is the antonomasias, in which two columns donate the antonomasia and the gender of a fictional character.
  ```
  name, gender
  小红, 0
  昊昊, 1
  ```
- `pre_prompts.txt` contains the basic relationships of first-order and second-order.
  ```
  父亲和儿子存在基因传承的父子关系，父亲比儿子大一辈，儿子称呼父亲为爸爸。
  父亲的父亲和父亲的儿子是祖孙关系，祖父比孙辈大两辈，孙辈应向祖父称呼爷爷。
  ```
- `derivation_rules.txt` states the common rules for deriving complex relationships.
  ```
  辈分长自己一辈或者两辈则已自己的父母进行类比称呼:
  长一辈，例如:妈妈的表哥表弟一表舅、爸爸的表姐妹一表姑姑或表姑妈
  长两辈，例如:妈妈的舅舅一舅姥爷、爸爸的姑姑一老姑
  长三辈，以自己父母类比加个“太”字例如:爸爸的爷爷一太爷爷、爸爸的外公一太外公、妈妈的外婆一太外婆
  ```
- `task_graph.txt` is the randomly constructed task graph in our experiments.
  - Process of constructing the task graph randomly.
    ![](https://github.com/NEU-DataMining/RoCar/figures/taskgraph.png)
  - Task graph.
    ![](https://github.com/NEU-DataMining/RoCar/figures/socialnetwork.png)
- `reasoning.txt` contains evaluation tasks in reasoning capability evaluation experiments.
- `memory.txt` contains evaluation tasks in memory capability evaluation experiments.

## Ackonwledgements
This was supported in part by the Data Mining Group at Northeastern University. Thanks to OpenAI, Anthropic, Baidu, Xunfei, and Tsinghua University for providing LLM applications and documentation support.

## Cite
``` bib
@misc{wang2023rocar,
      title={RoCar: A Relationship Network-based Evaluation Method to Large Language Models}, 
      author={Ming Wang and Wenfang Wu and Chongyun Gao and Daling Wang and Shi Feng and Yifei Zhang},
      year={2023},
      eprint={2307.15997},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
