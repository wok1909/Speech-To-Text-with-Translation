# OSSLab Final Project
## Youtube Link: https://www.youtube.com/watch?v=9Fy8kmOij7U

## Speech-To-Text-with-Translation

- This is Speach-To-Text-Translation constructed with DeepSpeech and Googletrans.
- This is a free open-source software using the two other open-source softwares consecutively.
- You can translate your speech into languges you want.
- DeepSpeech and Googletrans are both opensource and there are links below if you need.

    ▸ DeepSheech : https://github.com/touchgadget/DeepSpeech.git
    
    ▸ googletrans : https://github.com/ssut/py-googletrans.git

## Features

- You can choose your language to translate your speech.
- There are five preset languages that you can choose (Korean, Japanese, Chinese, Latin, Esperanto, and others).
- If you need other languages, check if the language you are finding exist in followed link. ([Language List])
- The input speech can be only English.
- If you want to change your translated language, then say "Change language".


## Installation

**Speech-To-Text-with-Translation requires python3+.**

**Deep Speech**

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

Transcribe three test files.
```sh
deepspeech --model deepspeech-0.9.3-models.tflite --scorer deepspeech-0.9.3-models.scorer --audio audio/2830-3980-0043.wav
deepspeech --model deepspeech-0.9.3-models.tflite --scorer deepspeech-0.9.3-models.scorer --audio audio/4507-16021-0012.wav
deepspeech --model deepspeech-0.9.3-models.tflite --scorer deepspeech-0.9.3-models.scorer --audio audio/8455-210777-0068.wav

```


For the microphone usage, run the comomad and change the default values of```defaults.ctl.card ``` and ```defaults.pcm.card ``` to 3.

```sh
sudo nano /usr/share/alsa/alsa.conf
```

```sh
defaults.ctl.card 3
defaults.pcm.card 3
```


Clone the git repository.
```sh
git clone https://github.com/wok1909/Speech-To-Text-with-Translation.git
pip3 install halo webrtcvad --upgrade
```

Now you are ready to use Deep Speech

**googletrans**

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

After installation, run to commad to run Speech-To-Text-With-Translation.
  
```sh
python3 DeepSpeech-examples/mic_vad_streaming/mic_vad_streaming.py -m deepspeech-0.9.3-models.tflite -s deepspeech-0.9.3-models.scorer
```

This command is only available in the directory ``` dspeech```. 
To make more easy and run the code in the hoome directory, follow the steps.

```sh
alias run='python3 dspeech/DeepSpeech-examples/mic_vad_streaming/mic_vad_streaming.py -m dspeech/deepspeech-0.9.3-models.tflite -s dspeech/deepspeech-0.9.3-models.scorer'
```

Also add the commad in ``` ~/.bashrc``` and use ``` source ./.bashrc```.

## Issues with Installation

Visit the Github and you can see more details about each installation

| Github | README |
| ------ | ------ |
| DeepSpeech | [DeepSpeech/Readme.md][DSpeech]|
| googletrans | [py-googletrans/Readme.rst][googletrans]|

Or you can contact me through the email below. 

## My Contribution 

- Deep Speech is a program that convert English speech to English text.
- googletrans is a module that translate text into another language text.
- I have revised Deep speech python code to translate the text that has been converted from speech into languages that users want.
- I have made the program to stop by saying "Shut Down" and made the program to change the language by saying "Change Language".
- For more details, watch the Youtube video provided above.


## Development

Want to contribute? Great!
Create a pull-request and I will checkout your code.
If you have anything to ask or suggest, contact me through my email!

**Contact Information: 21600437@handong.edu**

**Free Software, Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)

   [Language List]: <https://readthedocs.org/projects/py-googletrans/downloads/pdf/latest/>
   [DSpeech]: <https://github.com/touchgadget/DeepSpeech/blob/master/README.md>
   [googletrans]: <https://github.com/ssut/py-googletrans/blob/master/README.rst>

