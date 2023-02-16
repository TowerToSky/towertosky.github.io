---
layout: page
title: Audio Confuse
permalink: /datasets/audio_confuse
description: 音频诱发的困惑情绪识别脑电数据集
importance: 1
category: Datasets
# toc:

# - name: Abstract

# # if a section has subsections, you can add them as follows

# # subsections

# #   - name: Example Child Subsection 1

# #   - name: Example Child Subsection 2

# - name: Description
#   - name: Stimuli and Experiment
#   - name: Subjects
#   - name: Dataset Summary
# - name: Credits
# - name: Dataset access

# Below is an example of injecting additional post-specific styles

# If you use this post as a template, delete this _styles block


---
<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/confuse-experiment.png" title="confuse-experiment" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Abstract

The audio confuse dataset contains subjects' EEG signals when they were listening english audio clips. The audio clips are carefully selected to induce different types of emotion, which are confused, unconfused, and calm. Click here to know the details about the dataset.

## Description

If you are interested in using this dataset, you will have to print, sign and scan an EULA (End User License Agreement) and upload it via the email. We will then supply you with a username and password to download the data. Please head on over to the downloads page or click here for more details.

### Stimuli and Experiment

音频脑电情绪数据库是通过不同类型的音频诱导被试产生困惑和非困惑情绪，并采集相应的脑电图信号的情绪脑电数据库。该数据库采用的实验范式如图所示:

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/experiment.gif" title="experiment" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

被试在每次实验中都需要听一些音频，每段音频对应着一次数据记录。在每次试验开始前，受试者需要进行一段时间的冥想以保持接下来的精力集中。 实验开始之后，屏幕首先会呈现一个注视点，它提醒受试者有一段音频即将播放。音频在注视点出现1秒后开始播放。然后受试者开始根据音频内容回答问题， 回答问题的时间设置为5秒，被试回答完问题或持续时间超过5秒后，开始下一次音频播放。根据音频的内容，可以分为单词实验、句子实验和段落实验。

### Subjects
数据库中记录了14名受试者的脑电数据，但其中一名受试者的数据标签存在问题，因此只有13名受试者是有效数据。 受试者的年龄在21 ~ 35岁，平均24.5岁，标准差3.84岁，其中5名男性，8名女性。所有受试者均具有本科及以上学历，其中本科生3人，硕士研究生7人，博士研究生3人。 所有受试者均为右撇子，无智力或听力障碍，且均为中国人。

### Dataset Summary
下载数据集解压之后可以得到Audio_Confuse_Dataset文件夹，在该文件夹中包含14个从1-14编号的子文件夹， 分别存储14名受试者的数据。除此之外，文件夹中还有一个被试编码表文件，该文件记录了14名受试者的相关信息， 姓名和学号等敏感信息已经被提前删除。
以子文件夹1为例，在该文件夹下包含另外三个子文件夹，分别是：EEG、E-prime和质询。
其中EEG中存放了三段txt文件，命名为subject_id-1.txt, subject_id-2.txt, subject_id-3.txt, 1.txt是在做单词音频诱发实验时采集的脑电数据，2.txt和3.txt是句子和段落做诱发实验时采集到的脑电数据。 在txt文件中，前6行记录本次采集的相关信息，包括采样率相关内容，第7行开始正式记录脑电数据，每行脑电记录有11列，第1列是采样索引，最后一列是时间戳，倒数第二列是标记该时间点有无事件发生。如果是25120 表示发生了新事件。2-9列是记录的Fp1、Fp2、C3、C4、T5、T6、O1、O2八通道的脑电信号。通道位置符合下图所示10-20国际标准导联系统。
E-prime文件夹下有6个子文件，分别是：wordExp-subject_id-1.txt，wordExp-subject_id-1.edat2，sentExp-subject_id-2.txt，sentExp-subject_id-2.edat2， paraExp-subject_id-3.txt，paraExp-subject_id-3.edat2，分别记录了受试者在回答不同问题时的回答情况。.edat2文件和.txt文件区别在于.edat2文件 是记录的原始文件，只能通过E-prime软件直接打开，但是查看相关信息更直观，.txt打开方便但是不方便查看相关信息。通过每条回答下边Options.RESP、Options.CRESP和Options.ACC三个属性 可以确定对该段脑电信号记录的标签。其中Options.RESP是受试者回答的选项，Options.CRESP是正确答案的选项，Options.ACC是这道题受试者有没有回答正确。如果受试者回答正确，则该段脑电信号被标记为unconfused, 否则标记为confused。由于在每次实验开始前，受试者会被要求进行一段时间的冥想，这段时间的脑电记录被标记为calm。
在质询文件夹下同样有三个文件，分别是subject_id-表格-单词质询.xlsx，subject_id-文档-单句质询.docx，subject_id-文档-段落质询.docx，分别表示用于诱发受试者情绪的相关质询内容和顺序。
总体文件结构如下所示：

{% highlight html linenos %}
Audio_Confuse_Dataset
└─
├─EEG
├─subject_id-1.txt
    ├─subject_id-2.txt
    ├─subject_id-3.txt
├─E-prime
    ├─wordExp-subject_id-1.txt
    ├─wordExp-subject_id-1.edat2
    ├─sentExp-subject_id-2.txt
    ├─sentExp-subject_id-2.edat2
    ├─paraExp-subject_id-2.txt
    ├─paraExp-subject_id-2.edat2
├─质询
    ├─subject_id-表格-单词质询.docx
    ├─subject_id-文档-单句质询.docx
    ├─subject_id-文档-段落质询.docx
{% endhighlight %}

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.html path="assets/img/10-20system.png" title="10-20system" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

## Credits

First and foremost we'd like to thank the all(14) participants in this study for having the patience and goodwill to let us record their data. This dataset was collected by: Intelligent Interaction Laboratory @ Northwestern Polytechnical University

## Dataset access

To gain access to the dataset and download the files on this page, please download the license agreement below. The license agreement should be printed, signed, scanned and returned via email to xutao@nwpu.edu.cn with the subject of "RavenGaze account request". Upon receipt, a username, a password and a download link will be sent to download the data files below.

[The License Agreement](/assets/pdf/license_RavenGaze.pdf)

