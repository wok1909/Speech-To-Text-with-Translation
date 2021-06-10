# Speech-To-Text-with-Translation

# This is Speech-To-Text-Transltion constructed with DeepSpeech and Googletrans and they are run consecutively.
# DeepSheech : https://github.com/touchgadget/DeepSpeech.git
# googletrans : https://github.com/ssut/py-googletrans.git

# They are all open-source and free and not limitation of using them. 


# First install DeepSpeech

sudo apt install git python3-pip python3-scipy python3-numpy python3-pyaudio libatlas3-base
pip3 install deepspeech --upgrade
mkdir ~/dspeech
cd ~/dspeech
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.tflite
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/deepspeech-0.9.3-models.scorer
curl -LO https://github.com/mozilla/DeepSpeech/releases/download/v0.9.3/audio-0.9.3.tar.gz
tar xvf audio-0.9.3.tar.gz
source ~/.profile

# For the microphone usage, run the comomad and change the default values

sudo nano /usr/share/alsa/alsa.conf

defaults.ctl.card 3
defaults.pcm.card 3

git clone https://github.com/mozilla/DeepSpeech-examples
pip3 install halo webrtcvad --upgrade



# Now you are ready to use Deep Speech
# Now to install googletrans run the commad

pip3 install googletrans

# To check if you are ready to use googletrans run the codes in Python3

>>> from googletrans import Translator
>>> translator = Translator()
>>> translator.translate('안녕하세요.')
# <Translated src=ko dest=en text=Good evening. pronunciation=Good evening.>
>>> translator.translate('안녕하세요.', dest='ja')
# <Translated src=ko dest=ja text=こんにちは。 pronunciation=Kon'nichiwa.>
>>> translator.translate('veritas lux mea', src='la')
# <Translated src=la dest=en text=The truth is my light pronunciation=The truth is my light>
  
  
  
# If you are ready run to commad to run Speech-To-Text-With-Translation
  
python3 DeepSpeech-examples/mic_vad_streaming/mic_vad_streaming.py -m deepspeech-0.9.3-models.tflite -s deepspeech-0.9.3-models.scorer
  
  


  
  
  
  






