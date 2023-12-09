| Term | Description |
| - | - |
| <a id="cardinal"></a>Cardinal categories | Order/Priority does not matter. For e.g., <br>- Color: Red, Blue, Green, etc. <br>- City: New York, London, Paris, etc. <br>- Gender: Male, Female, Non-binary. <br>- Zip code: 636373, etc. <br> - User id: ... |  
| Categorical | In ML/DL, categorical columns represents types of data that can be divided into multiple categories. For e.g., <br><br><b>[Cardinal](#cardinal) categories</b>: Order does not matter<br>- Color: Red, Blue, Green, etc. <br>- City: New York, London, Paris, etc. <br>- Gender: Male, Female, Non-binary. <br>- Zip code: 636373, etc. <br> <br> <b>[Ordinal](#ordinal) categories</b>: Order matters<br>- Temperature: Low, Medium, High <br>- Ratings: 1, 2, 3, 4, 5. |
| Collaborative filtering | ... <br> For e.g.,, if customer A buys products 1 and 10, and customer B buys products 1, 2, 4, and 10, the engine will recommend that A buy 2 and 4 |
| Data augmentation | Synthetically generate variations of input data. Works well for different types of models, including images, text, etc. <br> For e.g., generating variations of input images, such as by rotating them or changing their brightness and contrast.  |
| Domain shift | Very common problem in ML.<br>The type of data that our model sees changes over time. <br> Also known as dataset shift, concept drift, or covariate shift, occurs when the distribution of the input data changes between the training phase and the testing (or deployment) phase. This can lead to a decrease in model performance, especially if the model is not updated or retrained to accommodate these changes, as the model has been originally trained on a different distribution of data. <br><br>e.g., a model trained to predict house prices based on data from 2010 might perform poorly when predicting prices in 2020, due to changes in the housing market over time (domain shift). <br><br>Types of domain shift:<br>- Covariate Shift<br>- Concept Drift<br>- Prior Probability Shift|
| Gradient Descent | Technique to change parameters of the NN ot make them "better". i.e., the mathematical function underneath to "learn" and do something useful. Often times, we try to minise the loss function (such as MAE). |
| Horizontal scaling | Also known as scaling out, is a method of adding more machines to a network to improve system performance and handle increased workload. This approach allows a system to serve more concurrent users by distributing the load across multiple servers or systems. | 
| Inference | Using trained model to get predictions |
| Learning rate |  One of the most important hyper-parameter to set when training a NN. Often, this learning rate is multiplied with gradients of the parameters to update the parameters (such that the loss would be minimised). |
| Learning rate schedule (or decay) | Decrease learning rate over the epichs as we train to avoid overshooting. |
| Model | Consists of two parts:<br>1. Architecture<br>2. Trained parameters |
| Neural Network | Just a mathematical function, but a very expressive one that can approximate any c omputable function, given enough parameters. |
| Object detection | Recognizing where objects in an image are, and highlight their locations and name of the each found object. <br> Variants: <br> - [Segmentation](#segmentation)|
| Object recognition | Computers recognizing what items are in an image. |
| Parameters | The values that are learnt by the NN model during training. |
| Rectified Linear Unit (ReLU) | A combination of <br>- linear function (multiplying things together and adding up like $ax+b$) and <br> - simply replacing all negative numbers with zero (like `max(x,0)`)|
| <a id="segmentation"></a>Segmentation | A variant of object detection, where every pixel is categorised based on what kind of object it's part of. Useful for self-driving vision. |
| Out-of-domain data|  Very common problem in ML. <br>Refers to the data that falls outside the range of the training dataset. In other words, it's data that the model has not seen before during its training phase. There may be data that our model sees in production which is very different to what it saw during training.  <br>e.g., if you train a model to recognize images of cats and dogs, and then you give it an image of a car, the car image would be considered out-of-domain data. |
| Sparse matrix | ... <br> e.g., A company like Amazon represents very purchase that has ever been made by its customers as a giant sparse matrix. i.e., a 2D vector with rows representing users and columns representing products.  |
| Tranfer learning | Instead of starting with random parameters for the NN model, starting with parameters of a different model that does something similar to what we want. |
| <a id="ordinal"></a> Ordinal categories | Order/ranking matters. For e.g., <br>- Temperature: Low, Medium, High <br>- Ratings: 1, 2, 3, 4, 5.
| Out-of-domain data | Information that falls outside of the specific knowledge, context, or data set that a model has been trained on. |
| Parameter | Useful for identifying how much memory a model needs. |

---
# FastAI specific
| Term | Description |
| - | - |
| `CategoryBlock` | |
| `DataBlock` | A fastai generic container/template to quickly build `Datasets` and [`DataLoaders`](#dataloaders) |
| <a id="dataloader"></a> `DataLoader` | A fastai object used to assemble data in a format suitable for training/validation/testing/etc.<br>`DataLoader` is a class that provides batches of a few items at a time to the GPU. When you loop through a DataLoader, fastai will give you 64 (by default) items at a time, all stacked up into a single tensor.
| <a id="dataloaders"></a>`DataLoaders` | A fastai class that stores multiple [`DataLoader`](#dataloader) objects you pass to it, normally a train and a valid, although it's possible to have as many as you like. |
| `ImageBlock` | | 