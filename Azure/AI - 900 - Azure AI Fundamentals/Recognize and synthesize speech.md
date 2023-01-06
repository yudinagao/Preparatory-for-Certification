# Recognize and synthesize speech

Speech recognition
- Acoustic model that converts the audio signal into phonemas
- Language model that maps phonemas to words, usually using statical algorithm that predicts the most probable sequence of words based on the phonemas

Synthesize Speech
- Text to be spoken
- The voice used

- system    tipically tokenizes the text
- broken down to individual words 
- assigning phonetic sounds
- breaks the phonetic transcription into prosidic units
    - such as phrases, clauses, or sentences
- to create phonemes that will be converted into audio

# Speech on Azure
 
## Speech to Text API

- real time or batch transcription of audio to text
- API based on the Universal Language model traing by Microsoft
- Model optimized for conversation and Dictation
- Create and train your models
    - including acoustics, language and pronunciation

## Text to Speech API

- specify the voice
- pre defines voices
- multiple languages
- regional pronunciations
- standard voices and neural voices
