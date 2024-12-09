# FINAL JOURNAL 
- I started this project by collecting over 15 hours of bird call audio recordings from the Macaulay library at Cornell. I had to email them for a media request and they were very gracious in allowing me to use their files for research purposes. I made sure there were no human voices and not a lot of silence in the audio files and eventually ended up with 9 hours of audio that I thought would be good. I wanted to minimize silence and non bird calls to optimize the data that the model was training on and minimize the possibility for training on unwanted features. 
- To use RAVE, I bounced between trying to start my own Colab from scratch and using the Colab provided in GitHub by IRCAM. The first time I ran the training, I let it run for 40 epochs (~2 hours) and then opened the .ts file in Max with the nn~ object. The model was able to match pitch pretty well but the timbre was definitely not bird like but there were some moments, especially in the higher register, that sounded a little like birds (maybe a seagull). The piece of music I chose to feed into my model was Queen of the Night aria from the magic flute because I think that the high register and variation of vocal articulation would be a good judge for the model I am trying to achieve. 
- Since the first run wasn’t what I was looking for. I kept resuming training until I got to Epoch 223. I would export some of the models and listen to them, but they were not really getting much better. For that reason, I decided to try training with a smaller dataset, prioritizing the loudest and most frequent bird calls. The second set was roughly 4 hours of wav files. I first listened to the model at epoch 65 and I was getting a similar result to the larger dataset except it had a harder time recreating pitch of the input. 
- I plan to try training again with an even more optimized dataset. I want to turn the samples into one shots of just the bird calls that last ~ 10 seconds compared to the minute long files I have in the set right now. I think shortening the files would force the model to train more on the calls themselves rather than the quiet or silent parts that might occur in the current dataset. I would like to implement this model either with RAVEVST or Max for live because I think A birdsong model would be an interesting compositional tool to use to blend the line between natural and electronic sounds in my music. 