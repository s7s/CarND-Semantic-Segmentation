# **Semantic Segmentation**


---

**The goals of this project are the following**:
* Load the pretrained vgg model
* Build a decoder part of the model
* Train and test a model architecture
* Tune the hyperparameters of the model
* Summarize the results with a written report


## Rubric Points
##### Here I will consider the [rubric points](https://review.udacity.com/#!/rubrics/989/view) individually and describe how I addressed each point in my implementation.

---
### Build the Neural Network

#### 1. Does the project load the pretrained vgg model?

Yes, I implemented `load_vgg` function `code_lines[33-57]` that load the pretrained vgg model.

#### 2. Does the project learn the correct features from the images?

Yes, I implemented `layers` function `code_lines[62-81]` that Create the layers for a fully convolutional network and build skip-layers( layers 3,4) using the vgg layers.

#### 3. Does the project optimize the neural network?

Yes, I implemented `optimize` function `code_lines[86-101]` that build the TensorFLow loss and optimizer operations.

#### 4. Does the project train the neural network?

Yes, I implemented `train_nn` function `code_lines[106-133]` that train neural network and print out the loss during training.



### Neural Network Training

#### 1.  Does the project train the model correctly?

Yes, On average, the model decreases loss over time. And here are the loss values over epochs:

|EPOCH|Loss|
|-------------|------------|
| EPOCH 1 ... | Loss = 0.218 |
| EPOCH 2 ... | Loss = 0.075 |
|EPOCH 3 ...|Loss = 0.116|
|EPOCH 4 ...|Loss = 0.269|
|EPOCH 5 ...|Loss = 0.263|
|EPOCH 6 ...|Loss = 0.066|
|EPOCH 7 ...|Loss = 0.302|
|EPOCH 8 ...|Loss = 0.023|
|EPOCH 9 ...|Loss = 0.051|
|EPOCH 10 ...|Loss = 0.090|
|EPOCH 11 ...|Loss = 0.202|
|EPOCH 12 ...|Loss = 0.058|
|EPOCH 13 ...|Loss = 0.136|
|EPOCH 14 ...|Loss = 0.055|
|EPOCH 15 ...|Loss = 0.016|
|EPOCH 16 ...|Loss = 0.053|
|EPOCH 17 ...|Loss = 0.081|
|EPOCH 18 ...|Loss = 0.073|
|EPOCH 19 ...|Loss = 0.087|
|EPOCH 20 ...|Loss = 0.073|


#### 2.  Does the project use reasonable hyperparameters?

Yes, the results have been good with this hyperparameters values:
* LEARNING_RATE=0.0005
* epochs=20
* batch_size=4

#### 3.  Does the project correctly label the road?

Yes, here are some of the resulted images:

<img src="./runs/1521160951.8885286/um_000012.png" alt="sets"  width="700"><br><br>

<img src="./runs/1521160951.8885286/um_000076.png" alt="sets"  width="700"><br><br>

<img src="./runs/1521160951.8885286/umm_000011.png" alt="sets"  width="700"><br><br>

<img src="./runs/1521160951.8885286/umm_000029.png" alt="sets"  width="700"><br><br>
