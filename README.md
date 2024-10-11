# Combined Dataset for Speech Emotion Recognition (SER)
- A collection of dataset consists of a total of 8 English speech emotion datasets.
- This dataset will help you create a generalized deep learning model for SER.
- Most of the data also includes text data for voice, which can be used for multimodal modeling.


&nbsp;
&nbsp;
&nbsp;


## Requirements
- Each dataset can be downloaded from the link below, and each data file must be located in [the appropriate folder](#project-structure).
- We use pandas profiling utilizing the [simple EDA](https://github.com/standing-o/Combined_Dataset_for_Speech_Emotion_Recognition/blob/master/SpeechEDA.ipynb).
```
conda install -c conda-forge ydata-profiling
```

&nbsp;
&nbsp;
&nbsp;


## Collection of Dataset
- A detailed description of each dataset is provided [here](https://github.com/standing-o/Combined_Dataset_for_Speech_Emotion_Recognition/blob/master/report.html).
  - This jupyter notebook generates [a single data frame](https://github.com/standing-o/Combined_Dataset_for_Speech_Emotion_Recognition/blob/master/speech_dataset.csv) containing the entire data paths and features.

### 1) [CREMA-D (Crowd Sourced Emotional Multimodal Actors Dataset)](https://github.com/CheyneyComputerScience/CREMA-D#crema-d-crowd-sourced-emotional-multimodal-actors-dataset)
> License: Open Database License, https://opendatacommons.org/licenses/odbl/1-0/
- Number of Dataset: 7442
- 48 male and 43 female actors between the ages of 20 and 74.
- A variety of races and ethnicities (African America, Asian, Caucasian, Hispanic, and Unspecified).
- `Emotion` 6 Classes: Anger, Disgust, Fear, Happy, Neutral, Sad
- In addition, it contains `Gender`, `Age` and `Emotion Level` features.

### 2) [MELD (Multimodal EmotionLines Dataset)](https://affective-meld.github.io/)
> Citation [1]: S. Poria, D. Hazarika, N. Majumder, G. Naik, R. Mihalcea,
E. Cambria. MELD: A Multimodal Multi-Party Dataset
for Emotion Recognition in Conversation. (2018)

> Citation [2]: Chen, S.Y., Hsu, C.C., Kuo, C.C. and Ku, L.W.
EmotionLines: An Emotion Corpus of Multi-Party
Conversations. arXiv preprint arXiv:1802.08379 (2018).

- Number of Dataset: Train, Test, Dev (We only used the train data.)
- MELD has 1400+ dialogues and 13,000+ utterances from 'Friends.
- `Emotion` 7 Classes: Anger, Disgust, Sadness, Joy, Neutral, Surprise and Fear
- `Sentiment`: Positive, Negative and Neutral

### 3) [MLEnd](https://www.kaggle.com/datasets/jesusrequena/mlend-spoken-numerals)
> The MLEnd datasets have been created by students at the School of Electronic Engineering and Computer Science, Queen Mary University of London.

- 31 nationalities and 42 unique languages, 154 speakers
- Each audio recording corresponds to one English numeral (from "zero" to "billion") that is read using different intonations
- Number of Dataset: 32654
- `Emotion` 4 Classes: Neutral, Bored, Excited and Question
- It contains `Nationality` feature.

### 4) [RAVDESS (Ryerson Audio-Visual Database of Emotional Speech and Song)](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio)
> Citation: "The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)" by Livingstone & Russo is licensed under CC BY-NA-SC 4.0.

- 24 professional actors (12 female, 12 male), two lexically-matched statements in a neutral North American accent. 
- Number of Dataset: 1440
- `Emotion` 7 Classes: Calm, Happy, Sad, Angry, Fearful, Surprise and Disgust
- Emotional `Intensity`: Normal, Strong

### 5) [SAVEE (Surrey Audio-Visual Expressed Emotion)](https://www.kaggle.com/datasets/ejlok1/surrey-audiovisual-expressed-emotion-savee)
> License: Data files © Original Authors | Authors: Philip Jackson and Sanaul Haq

- Four native English male speakers, aged from 27 to 31 years
- A total of 120 utterances per speaker, 15 TIMIT sentences per emotion: 3 common, 2 emotion-specific and 10 generic sentences
- `Emotion` 7 Classes: Anger, Disgust, Fear, Happiness, Sadness and Surprise

### 6) [TESS (Toronto emotional speech set)](https://www.kaggle.com/datasets/ejlok1/toronto-emotional-speech-set-tess)
> License: Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0), https://creativecommons.org/licenses/by-nc-nd/4.0/

- 200 target words were spoken in the carrier phrase "Say the word _' by two female actresses (aged 26 and 64 years).
- `Emotion` 7 Classes: Anger, Disgust, Fear, Happiness, Pleasant Surprise, Sadness, and Neutral
- It contains `Age` and `Gender` features.

### 7) [Emotional Voice Conversion: Theory, Databases and ESD](https://hltsingapore.github.io/ESD/download.html)
> Citation: Kun Zhou, Berrak Sisman, Rui Liu and Haizhou Li, "Seen and unseen emotional style transfer for voice conversion with a new emotional speech dataset" ICASSP 2021-2021 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)

- 350 parallel utterances spoken by 10 native English and 10 native Mandarin speakers.
  - We only used English.
- `Emotion` 5 Classes: Neutral, Happy, Angry, Sad and Surprise

### 8) [JL Corpus](https://www.kaggle.com/datasets/tli725/jl-corpus)
> License: CC0: Public Domain, https://creativecommons.org/publicdomain/zero/1.0/

> Citation: Jesin James, Li Tian, Catherine Watson, "An Open Source Emotional Speech Corpus for Human Robot Interaction Applications", in Proc. Interspeech, 2018.

- Emotional speech corpus with balanced New Zealand English vowels, encompassing 5 primary and 5 secondary emotions.
- `Emotion` 10 Classes: Angry, Anxious, Apologetic, Assertive, Concerned, Encouraging, Excited, Happy, Neutral and Sad
- In addition, it contains a `Gender` feature.

## Project Structure

```shell
├── dataset                      # Not contained in this repository
│   ├── crema-d                  # CREMA-D dataset
│   ├── meld                     # MELD dataset
│   ├── mlend                    # MLEnd dataset
│   ├── ravdess                  # RAVDESS dataset
│   ├── savee                    # SAVEE dataset
│   ├── tess                     # TESS dataset
│   ├── esd                      # Emotional Voice Conversion: Theory, Databases and ESD dataset
│   └── jl-corpus                # JL Corpus Dataset
├── MakeEngSpeechDataset.ipynb   # Make a Dataframe Including 8 Dataset
├── SpeechEDA.ipynb              # EDA using Pandas Profiling
├── speech_dataset.csv           # Main Dataset
└── report.html                  # EDA Report
```

