### Training a RAVE Generative Model on Bird Calls
Gibran Mobarak 
# Abstract
This project explores the use of the RAVE (Real-time Audio Variational autoEncoder) generative AI style transfer model to synthesize bird calls from a input audio source for creative and compositional purposes. Using  a range of bird call audio data from Cornell University's Macaulay Library, the project aims to develop a model capable of generating sounds that blur the boundaries between natural bird calls and electronic music.
# Data Collection and Preprocessing
The dataset consisted of over 15 hours of bird call recordings sourced from the Macaulay Library. After obtaining permission for research use, I curated and trimmed the recordings to exclude human voices and reduce silent segments, resulting in a refined dataset of approximately 9 hours. This preprocessing step aimed to optimize the model's training by minimizing noise and irrelevant features in the data.
# Training Setup
The RAVE model, developed primarily by Antoine Caillon at IRCAM, was utilized via a Google Colab notebook using open source code available on github. Initial training was conducted for 40 epochs (~2 hours). The output model was evaluated by integrating the resulting .ts file with Max/MSP's nn~ object, enabling audio synthesis testing in real time through a visual interface. While the model exhibited accurate pitch reproduction, its timbre lacked resemblance to bird calls. Notable moments, particularly in higher registers, hinted at birdlike qualities, albeit closer to seagull-like sounds.
To evaluate the model’s generative capabilities, I input the "Queen of the Night" aria from The Magic Flute. This piece was chosen for its wide pitch range and dynamic vocal articulations, providing a rigorous test for the model’s ability to adapt and generate expressive timbres.
# Iterative Refinement
Following the initial training, the model was further trained to epoch 223, with periodic evaluations. Despite extended training, the generative quality showed limited improvement, prompting a revision of the dataset. A smaller, more focused dataset (~4 hours) was created, prioritizing prominent and frequent bird calls. This reduced dataset aimed to further optimize training by isolating key features of the bird calls. However, this approach led to decreased pitch reproduction accuracy, suggesting potential over-reduction in data diversity.
# Future Directions
To enhance the model’s performance, future iterations will focus on further optimizing the dataset. Specifically, I plan to create shorter, one-shot samples (~10 seconds) of isolated bird calls, replacing the current longer (~1 minute) audio files from the original dataset. This adjustment aims to concentrate training on bird call features while minimizing interference from silence, human or environmental noise.
Ultimately, I intend to integrate the trained model into compositional workflows using tools such as RAVE VST or Max for Live. The bird call model has potential as a unique compositional tool, merging organic sounds with electronic textures and offering novel avenues for music creation.
# Conclusion
This project demonstrates the challenges and possibilities of training generative audio models on unconventional datasets like bird calls. While the initial results indicate room for improvement, iterative training and dataset optimization present promising directions for refining the model's capabilities and unlocking its creative potential.
