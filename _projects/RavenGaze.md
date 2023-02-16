---
layout: page
title: RavenGaze
permalink: /datasets/RavenGaze
description: 瑞文实验诱发的注视估计数据集
importance: 4
category: Datasets
---

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/expriment_process.jpg" title="expriment process" class="img-fluid rounded z-depth-1" %}
    </div>s
</div>

# Abstract

One major challenge in appearance-based gaze estimation is the lack of high-quality labeled data. Establishing databases or datasets is a way to obtain accurate gaze data and test methods or tools. However, the methods of collecting data in existing databases are designed on artificial chasing target tasks or unintentional free-looking tasks, which are not natural and real eye interactions and cannot reflect the inner cognitive processes of humans. To fill this gap, we propose the first gaze estimation dataset collected from an actual psychological experiment by the eye tracker, called the RavenGaze dataset. We design an experiment employing Raven's Matrices as visual stimuli and collecting gaze data, facial videos as well as screen content videos simultaneously. Thirty-four participants were recruited. The results show that the existing algorithms perform well on our RavenGaze dataset in the 3D and 2D gaze estimation task, and demonstrate good generalization ability according to cross-dataset evaluation task. RavenGaze and the establishment of the benchmark lay the foundation for other researchers to do further in-depth research and test their methods or tools.

## Description

### Stimuli and Experiment

We used the 48-question from Raven Progressive Matrices (RPM) as the subject's visual stimuli. In addition, to ensure subjects are not distracted as much as possible during the task time, we set answer time for questions(15s) shorter than the average time to work out the questions. The procedure of the experiment is shown in Fig.1.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/1-experiment_procedure.png" title="1-experiment_procedure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Fig. 1. The procedure of experiment
</div>

Before each subject starts the investigation, first, the eye tracker is calibrated the gaze of the current subject to reduce the gaze error of the collection process. Then ten landscape pictures help the subject calm down and enter the test state. After that, it begins the test, which includes 48 questions. We set each question to have a maximum answering time of 15 seconds. The subject must press the button corresponding to the answer option preset by the program within the answering time to complete the question and automatically jump to the next question. If the subject does not meet the answer within the set time, it will automatically jump to the next question. Before jumping to the next question, a calibration break is set to ensure high-quality gaze data. It is a fixation point that appeared in the center of the screen for 0.5 seconds, and subjects were asked to focus on this fixation point as much as possible.During the answering process, the program simultaneously records the facial video, screen video, and eye movement data of each subject during completing the 48 reasoning questions.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/2-Experiment_setting.png" title="1-2-Experiment_setting" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Fig. 2. Experiment setting
</div>

The experiment setting is shown in Fig. 2, and the visual stimuli materials are displayed on a 27-Inch monitor. The subjects’ videos are captured from a commercial webcam fixed on the top of the screen. Logitech C270 HD Webcam is chosen, since it is one of low-cost and most widely used webcam, supporting 1280 × 720 video recording with lightcorrection technology.

### Dataset Summary

We collected gaze data from a total of 34 subjects(18 female and 16 male), with 22 wearing glasses and 12 having normal vision. Three subjects' gaze data were screened out due to improper experimental operation. The data were collected under well-lit indoor conditions, where the sampling rate of face video was 30Hz, and the sampling rate of Tobii Pro Nano eye tracker was 60Hz. The time for each subject to complete RMP test is about 8-11 minutes. The entire dataset contains 31 subjects' facial videos with a total length of 309 minutes. There are 556,476 images in total, some face image examples are shown in Fig.3.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/3-face_image.png" title="3-face_image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Fig. 3. Face image from the dataset
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/4-densityHeatMap.png" title="4-densityHeatMap" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Fig. 4. Gaze angle and gaze point distribution
</div>

The angle range of the horizontal direction is (-10°, +10°), and the angle of the vertical direction is (-12°, 12°), which is smaller than another gaze dataset. It also means that RavenGaze places higher demands on the recognition algorithms.

## How to use

If you are interested in using this dataset, you will have to print, sign and scan an EULA (End User License Agreement) and upload it via the dataset request form. We will then supply you with a username and password to download the data.

## Credits

First and foremost we'd like to thank the all(34) participants in this study for having the patience and goodwill to let us record their data. This dataset was collected by: Intelligent Interaction Laboratory @ Northwestern Polytechnical University

## Dataset access

To gain access to the dataset and download the files on this page, please download the license agreement below. The license agreement should be printed, signed, scanned and returned via email to <a href="mailto:xutao@nwpu.edu.cn">xutao@nwpu.edu.cn</a> with the subject of "RavenGaze account request". Upon receipt, a username, a password and a download link will be sent to download the data files below.

[The License Agreement](/assets/pdf/license_RavenGaze.pdf)
