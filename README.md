# AI Music

This repo contains records of my journey studying AI applied to the music field. To help me guide through the field I will use and application/project based approach following the recomendations from this **Valerio Velardo**'s [video](https://youtu.be/d3e-f7V-hR4).

## Projects

This section shows my undersanting of the projects that I am targeting to study/implement:

### Music Genre Classifier

In this system the user should provide an mp3 file with at least **X** seconds and the system returns the music genre.

Features:
* Open any MP3 file format
* REST API

Datases:
* [GTZAN dataset](https://www.kaggle.com/andradaolteanu/gtzan-dataset-music-genre-classification)
* [Million Song Dataset](http://millionsongdataset.com/)
* [Million Song Dataset Benchmarks](http://www.ifs.tuwien.ac.at/mir/msd/)

### Loop Recombination System

This system should be able to recombinate loop samples to generate sensible music. 

Features:
* Import sample dataset and preprocess to figure general features like: pitch, contour, key, bpm, danceability, style, instrument, spectrogram, MFC
* Define general characteristics of final product like: length, mood, style, use voice, bpm
* Select/remove instruments
* Rules tweaking for fine tuning
* ML: How to measure good tracks?
* Extra: PWA for user interface

Datasets:

* [Freesound Loop Dataset](https://arxiv.org/abs/2008.11507)
* [Freesound Labs Dataset](http://labs.freesound.org/datasets/)
* [Freesound](https://freesound.org/)

### Audio ML Pipeline

This project aims at automating ML pipelines for Audio ML from data gathering through deploy.

Features:

* Should support standard pipelines: preprocess, training, evaluation, deploy
* Support at least two ML frameworks: TensorFlow, PyTorch, FastAI
* Deploy to AWS and GCP using Containers


### Music Sumarization

This project extract the most important sections of one music track into one mixed mp3

Features

* Users will provide mp3 file and get back summarized 30 seconds mp3
* Model understands Chorus, Verse, Bridge and remarkable sections
* EXTRA: Summary could be of arbitrary length

### Polifonic Piano Accompaniment

The Accompaniment project get as input one melody line and generate a sensible piano/guitar accompaniment

Features:

* Get MIDI file and generate back MIDI file
* Generate simple chord progressions
* Configure geral style/genre of accompaniment
* EXTRA: Multi instrument (Loop Recombination System?)
* EXTRA: Use GAN
* EXTRA: Get melody from WAV file

### Music Recommender System

This system should recommend tracks for user based on collaborative filtering and content based filtering

Features

* Generate Playlist of *n* tracks
* Recommend on the fly: next track based on previous one + signals (skip, dislike, like, etc)
* EXTRA: Ensamble engine using both filtering approaches
* EXTRA: Personality based RecSys (Use Loop RecEng tracks as base?)

### Noise Cancelling System

This system will remove noise from audio tracks. It should be able to remove only noise but also works as a full noise supression system. Possible approaches are **wavelets** and **variational auto encoders**

Features

* Work in batch in audio tracks
* User defined noise threshold
* EXTRA: Work in realtime