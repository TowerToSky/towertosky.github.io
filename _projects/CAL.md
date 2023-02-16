---
layout: page
title: CAL
permalink: /datasets/cal
description: 瑞文实验诱发的情绪识别脑电数据集
importance: 2
category: Datasets
---

## Abstract
Confusion is the core emotion in the learning process, affecting learners' engagement and cognitive load level and determining whether frustration and boredom occur. This work proposes and presents the CAL database - a database of EEG signals for Confusion Analysis in Learning. CAL is the first database for investigating learning emotion via physiological signals to our best knowledge. CAL has three contributions, 1. design a new stimuli experiment to improve induction efficiency and accuracy. 2. propose a subjective and objective joint labeling strategy to solve the noisy labels issue. 3. provide an available dataset with benchmark results based on conventional and end-to-end machine learning approaches. We encourage other researchers to use it for testing their proposed methods or tools for recognizing students' confused states in learning. Click here to know the details about the dataset.

### Stimuli and Experiment

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/1-experiment_procedure.png" title="1-experiment_procedure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

The experiment system comprises three parts: EEG collector, confusion inducer, and data storage, as shown in Figure.3. We employed OpenBCI as the EEG collector in this work, due to its lowcost, high-quality bio-sensing hardware for brain-computer interfacing. It has eight channels (Fp1, Fp2, C3, C4, T5, T6, O1, O2) and a high sample rate (250Hz) at an affordable price, providing the possibility of large-scale collection of EEG signals in learning study and application. We use one desktop to induce confused states and a laptop to connect with the EEG collector and store the data.We used E-prime , a software for behavioral and psychological research, to generate the stimuli materials and interaction. It also sent trigger signals for segmenting trials. We redeveloped the firmware and software of the OpenBCI Cyton Board, making it receive the trigger signals from DB25. When storing the data, the EEG waves were real-time sync visualized. This visualization helps testers monitor the experiment.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/fig3.jpg" title="fig3" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Subjects
A total of 25 subjects participated in this experiment. We obtained 23 subjects’ data because the unexpected equipment problem made failed collecting for two persons. The ages were between 20 and 47 (Mean = 24.48, SD = 6.36); the male to female ratio is roughly half to half (12:11). The education backgrounds covered middle school, undergraduate, master, and doctoral degrees, and the major included computer science, microelectronics, bioengineering, and British and American literature. All participants were in good health and had normal vision without any history of brain injury or mental illness. Before the experiment, each subject signed an ultimate consent form. Then, the experiment testers would explain the experiment’s purpose, process, and precautions and inform subjects that it will not cause any harm. As shown in Figure, we first presented the manipulation instruction. When subjects were ready, they watched ten non-confused scene pictures, each of which lasted ten seconds. Next to this, they viewed and performed 48 tests, each of which lasted a maximum of 15 seconds. Finally, the subjects filled out the questionnaires.

### Dataset Summary
The Dataset consists 23 subject' data(failed subject 1 and subject 6), and each subject has 49 files. There are five labels, confused,non-confused,guess,think-right and rest. And the data labeled undefined is wasted. The data sample rate is 250Hz. The EEG cap according to the international 10 - 20 system for 8 channels is shown below: "Fp1", "Fp2", "C3", "C4", "T5", "T6", "O1", "O2"

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/10-20system.png" title="10-20system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>


## How to use
If you are interested in using this dataset, you will have to print, sign and scan an EULA (End User License Agreement) and upload it via the dataset request form. We will then supply you with a username and password to download the data.

## Credits
First and foremost we'd like to thank the all(25) participants in this study for having the patience and goodwill to let us record their data. This dataset was collected by: Intelligent Interaction Laboratory @ Northwestern Polytechnical University

## Dataset access

To gain access to the dataset and download the files on this page, please download the license agreement below. The license agreement should be printed, signed, scanned and returned via email to <a href="mailto:xutao@nwpu.edu.cn">xutao@nwpu.edu.cn</a> with the subject of "RavenGaze account request". Upon receipt, a username, a password and a download link will be sent to download the data files below.

[The License Agreement](/assets/pdf/license_RavenGaze.pdf)

