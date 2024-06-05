This repository contains the code and data related to LERT. The code section includes the implementations of the Devign and Reveal models in LERT. The data section includes training and testing data from BigVul, as well as data enhanced from GPT-4, Vgx, and Juliet.

--Devign_modified:
This directory contains the implementation of the Devign model. Usage:

bash
python [-c|-e|-p] main.py

These options are used for generating the code fragment's CPG, generating embeddings, and training and testing, respectively. The data in the paper is derived from repeating the experiment 10 times and taking the arithmetic mean of the results.

--Reveal_modified:
This directory contains the implementation of the Reveal model. Usage:

bash
python [-c|-e|-pS|-p] main.py

These options are used for generating the code fragment's CPG, generating embeddings, training and testing with the SMOTE mechanism, and training and testing without the SMOTE mechanism, respectively. The data in the paper is derived from repeating the experiment 10 times and taking the arithmetic mean of the results.

--data:
This directory contains the data used in the experiments. Specifically:

bigvul_sampled.json: The dataset used for the baseline.
chatgpt.json: The baseline dataset augmented with data generated using GPT-4.
juliet.json: The baseline dataset augmented with data from some defect types in the Juliet dataset.
vgx.json: The baseline dataset augmented with 1370 randomly selected entries from the Vgx dataset (as the Vgx dataset lacks defect type information).
