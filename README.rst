# OSSLab Final Project
## Speech-To-Text-with-Translation

Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

- This is Speach-To-Text-Translation constructed with DeepSpeech and Googletrans.
- You can translate your speech into languges you want.
- DeepSpeech and Googletrans are both opensource and there are links below if you need.

▸ DeepSheech : https://github.com/touchgadget/DeepSpeech.git
▸ googletrans : https://github.com/ssut/py-googletrans.git

## Features

- There are 5 preset languages that you can choose (Korean, Japanese, Chinese, Latin, Espa).
- If you need other languages, check if the language you are finding exist in followed link. (https://readthedocs.org/projects/py-googletrans/downloads/pdf/latest/)

Markdown is a lightweight markup language based on the formatting conventions
that people naturally use in email.
As [John Gruber] writes on the [Markdown site][df1]

> The overriding design goal for Markdown's
> formatting syntax is to make it as readable
> as possible. The idea is that a
> Markdown-formatted document should be
> publishable as-is, as plain text, without
> looking like it's been marked up with tags
> or formatting instructions.

## Installation

Speech-To-Text-with-Translation requires python3+.

Install Guide

```sh
sudo apt install git python3-pip python3-scipy python3-numpy python3-pyaudio libatlas3-base
pip3 install deepspeech --upgrade
mkdir ~/dspeech
cd ~/dspeech
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.tflite
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.scorer
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/audio-0.9.3.tar.gz
tar xvf audio-0.9.3.tar.gz
source ~/.profile
```

For the microphone usage, run the comomad and change the default values.

```sh
sudo nano /usr/share/alsa/alsa.conf
```

```sh
defaults.ctl.card 3
defaults.pcm.card 3
```


```sh
git clone https://github.com/mozilla/DeepSpeech-examples
pip3 install halo webrtcvad --upgrade
```

```sh
git clone https://github.com/mozilla/DeepSpeech-examples
pip3 install halo webrtcvad --upgrade
```


Now you are ready to use Deep Speech

To install googletrans run the commad

```sh
pip3 install googletrans
```


To check if you are ready to use googletrans run the codes in Python3

```sh
>>> from googletrans import Translator
>>> translator = Translator()
>>> translator.translate('안녕하세요.')
# <Translated src=ko dest=en text=Good evening. pronunciation=Good evening.>
>>> translator.translate('안녕하세요.', dest='ja')
# <Translated src=ko dest=ja text=こんにちは。 pronunciation=Kon'nichiwa.>
>>> translator.translate('veritas lux mea', src='la')
# <Translated src=la dest=en text=The truth is my light pronunciation=The truth is my light>
```

If you are ready run to commad to run Speech-To-Text-With-Translation
  
```sh
python3 DeepSpeech-examples/mic_vad_streaming/mic_vad_streaming.py -m deepspeech-0.9.3-models.tflite -s deepspeech-0.9.3-models.scorer
```

## Issues with Installation

Visit the Github and you can see more details about each installation

| Github | README |
| ------ | ------ |
| DeepSpeech | [DeepSpeech/Readme.md][DSpeech]|
| googletrans | [py-googletrans/Readme.rst][googletrans]|

## My Contribution 


## Development

Want to contribute? Great!





**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [DSpeech]: <https://github.com/touchgadget/DeepSpeech/blob/master/README.md>
   [googletrans]: <https://github.com/ssut/py-googletrans/blob/master/README.rst>

