# Awesome Large Language Model Knowledge Update Paper

## Paper

### Survey & Framework

- [A Survey on Knowledge Distillation of Large Language Models](https://arxiv.org/pdf/2402.13116). Arxiv 2402.
  - Paper List: [GitHub - Tebmer/Awesome-Knowledge-Distillation-of-LLMs](https://github.com/Tebmer/Awesome-Knowledge-Distillation-of-LLMs?tab=readme-ov-file#reinforcement-learning)
- [EasyEdit: An Easy-to-use Knowledge Editing Framework for Large Language Models](https://arxiv.org/pdf/2308.07269). ACL 2024 System Demonstration Track.
  - Code: [GitHub - zjunlp/EasyEdit](https://github.com/zjunlp/EasyEdit)

### Paper List

- [ROME](https://github.com/kmeng01/rome), [MEND](https://github.com/eric-mitchell/mend), [WISE](https://github.com/zjunlp/EasyEdit/tree/main/easyeditor/models/wise), ...

- (FT) [When Scaling Meets LLM Finetuning: The Effect of Data, Model and Finetuning Method](https://openreview.net/pdf?id=5HCnKDeTws). ICLR 2024.
  - Google DeepMind, Google Research.
- (SFT) [Injecting New Knowledge into Large Language Models via Supervised Fine-Tuning](https://arxiv.org/pdf/2404.00213). Arxiv 2404.
  - Microsoft
  - Task: knowledge injection
  - Dataset: six Wikipedia articles about sporting events
- (KD) [Distilling the knowledge in a neural network](https://arxiv.org/pdf/1503.02531). Arxiv 1503.
- (SeqKD) [Sequence-level knowledge distillation](https://aclanthology.org/D16-1139.pdf). EMNLP 2016.
  - Code: [GitHub - harvardnlp/seq2seq-attn](https://github.com/harvardnlp/seq2seq-attn)
- (SeqKD) [LIMA: Less is more for alignment](https://openreview.net/pdf?id=KBMOKmX2he). NeurIPS 2023.
  - Task: instruction tuning
  - Dataset: 1000 sequences from different sources
  - Model: LLaMa 65B
  - Insight: Almost all knowledge in large language models is learned during pretraining, and only limited instruction tuning data is necessary to teach models to produce high quality output.
- (Context Distillation) [Propagating Knowledge Updates to LMs Through Distillation](https://proceedings.neurips.cc/paper_files/paper/2023/file/932147114c48f8b04d41aebc0c631158-Paper-Conference.pdf). NeurIPS 2023.
  - Code: [Github - shankarp8/knowledge_distillation](https://github.com/shankarp8/knowledge_distillation)
  - Task: propagate knowledge updates
  - Dataset: ECBD, ENTITY INFERENCES
  - Model: GPT-NEO-1.3B, GPT2-XL.
- (ReverseKD) [MiniLLM: Knowledge distillation of large language models](https://openreview.net/pdf?id=5h0qf7IBZZ). ICLR 2024.
  - Code: [Github - microsoft/LmOps](https://github.com/microsoft/LMOps/tree/main/minillm)
  - Task: instruction-following setting
  - Dataset: Dolly, SlefInst, Vicuna, S-NI, UnNI.
  - Model: (teacher) GPT-2 1.5B, OPT 13B, Llama 13B. (student) GPT-2 120M, 340M, 760M; OPT 1.3B, 2.7B, 6.7B; Llama 7B.
- (PDKD) [Direct Preference Knowledge Distillation for Large Language Models](https://arxiv.org/pdf/2406.19774). Arxiv 2406.
  - Code: [aka.ms](https://aka.ms/dpkd)
  - Task: instruct tuning
  - Dataset: DollyEval, Self-Inst, S-NI (SuperNatural-Instruction).
  - Model: (teacher) GPT-2, OPT 13B. (student) GPT-2 with 120M and 340M, OPT with 1.3B.



## Datasets

We collected datasets that have been used for knowledge update tasks in previous work.

- WikiData
  - [Evaluating the ripple effects of knowledge editing in language models](https://watermark.silverchair.com/tacl_a_00644.pdf?token=AQECAHi208BE49Ooan9kkhW_Ercy7Dm3ZL_9Cf3qfKAc485ysgAAA0UwggNBBgkqhkiG9w0BBwagggMyMIIDLgIBADCCAycGCSqGSIb3DQEHATAeBglghkgBZQMEAS4wEQQMRRkOhp-zQOR6XWlJAgEQgIIC-POog9kqzU4jor8z8AicNcSEg8zPjZQQmEGvfw2OOx1usxyRcRMMRJgvdgeSDUkLsZYGW68dkFRcYTC8OubBqs1XtK8YzlLIpGWBSxrloWZjO1ocBtHGYIt01BjOLaQ0b9UNJb7QvEUyPUJq9g3w7h8P3-E7luonggqKKEmusoHJAbgwb_n3px_AmatfY-gtOxS0leEH3TD0uf4hlie0TK4q7ERZFEpM3V2yEvfPL2-Rv-I703v8aJ51_ar7x64lLxcdx2CP0jkuOZenyDneJ894EJVr-GvrxdGFzoeJOrcIVzBbXBxXnC28I-7LsXqJYV5sEkuU7vFSQYJoIeJ33H3IFd-QFcgM2X2tdnnjUNOhCcKsdftcya120bi2ug7DMzIbfXau2xqYJSiMjeRu61aUko9x0Qk0n_Ij-E04RB2fsslogFlY8Cz7BarnYJX5ZPZOHEcGViGVidKuBrhP3wzUNBCkavtXugvuKfmNJPRKZwEa59DAzSvrTf3yqHZ7UnQUVZTRN0XefaDAnLWJLrEySDPABqFYVkqwfBoAOYEORXo7tIhfQhUCNm0DpF8D8b6amoV8WPzj0GjzqA1sROAYu9ONyjEADfp3cYo6hTz9lD05VHnUrIPZFsVedkIjVjXk13kHJJ8dMzi9uIdbCpwgHVgE9o1t9iCJB-N_TFLgYHEr25wt6qYh8PsBjBwuSv1tdSdjFChyvBwsdFOPFnJn-oqI3rd8TofsxsGio_xg7DJwgdYsV38pvnYBONZ9lMpzVMeHvYWdL2jPH_GoMS4oAG2oG4f9zwAxGJiepDCwIjDxSkcd_nfOikCdB1EdfBffEmQ0IZts6KVlJtX1VV5NU-B8AnPvurCjakj2ZyfXcVB-W98pYA6H3q6NGhlrNucfs9cXqjJOsh-6iL4TDLjlymgsevpc8HtHgOl79JYHVY2m7Utgfk7-dWGqqpdL0cSsYSQO0J86Zd1i4GD0a3uQDuSRdjpsPN-Vzzn05lB6huqfJWdE8U8). ACL 2024.
  - Time: a range of 250 days after July 2022.
- ECBD: Entity Cloze By Date
  - [Entity Cloze By Date: What LMs Know About Unseen Entities](https://arxiv.org/pdf/2205.02832). NAACL 2022
  - Time: 2017 to 2021
- ENTITY INFERENCES
  - [Can LMs Learn New Entities from Descriptions? Challenges in Propagating Injected Knowledge](https://arxiv.org/pdf/2305.01651). ACL 2023.
  - Time: real entity with definition sentences from the 2020 and 2021 subsets of ECBD + fake people information
- Recent sporting events in Wikipedia articles
  - [Injecting New Knowledge into Large Language Models via Supervised Fine-Tuning](https://arxiv.org/pdf/2404.00213). Arxiv 2404.
  - Time: 5 events in 2023, 1 event in 2018.



## Notes

#### Training Stages

- Pre-training
  - unsupervised pretraining from raw text, to learn general-purpose representations
- Fine-tuning
  - Instruct tuning and reinforcement learning
  - better align to end tasks and user preferences

reference to  [LIMA: Less is more for alignment](https://openreview.net/pdf?id=KBMOKmX2he). 

- More precise training paradigm?
  - knowledge edit/propagation/distillation/update
