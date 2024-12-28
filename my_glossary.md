| Term | Description |
| - | - |
| Baseline | A simple model which we are condifent should perform reasonably well. It should be very simple to implement, and very easy to test each of our improved ideas. |
| Broadcasting | PyTorch<br>- It will automatically expand the tensor with the smaller rank to have the same size as the one with the larger rank. Broadcasting is an important capability that makes tensor code much easier to write. <br>- For e.g., `tensor([1,2,3]) + tensor(1)` will result in `tensor([2,3,4])`.|
| <a id="cardinal"></a>Cardinal categories | Order/Priority does not matter. For e.g., <br>- Color: Red, Blue, Green, etc. <br>- City: New York, London, Paris, etc. <br>- Gender: Male, Female, Non-binary. <br>- Zip code: 636373, etc. <br> - User id: ... |  
| Categorical | In ML/DL, categorical columns represents types of data that can be divided into multiple categories. For e.g., <br><br><b>[Cardinal](#cardinal) categories</b>: Order does not matter<br>- Color: Red, Blue, Green, etc. <br>- City: New York, London, Paris, etc. <br>- Gender: Male, Female, Non-binary. <br>- Zip code: 636373, etc. <br> <br> <b>[Ordinal](#ordinal) categories</b>: Order matters<br>- Temperature: Low, Medium, High <br>- Ratings: 1, 2, 3, 4, 5. |
| Collaborative filtering | ... <br> For e.g.,, if customer A buys products 1 and 10, and customer B buys products 1, 2, 4, and 10, the engine will recommend that A buy 2 and 4 |
| Data augmentation | Synthetically generate variations of input data. Works well for different types of models, including images, text, etc. <br> For e.g., generating variations of input images, such as by rotating them or changing their brightness and contrast.  |
| Domain shift | Very common problem in ML.<br>The type of data that our model sees changes over time. <br> Also known as dataset shift, concept drift, or covariate shift, occurs when the distribution of the input data changes between the training phase and the testing (or deployment) phase. This can lead to a decrease in model performance, especially if the model is not updated or retrained to accommodate these changes, as the model has been originally trained on a different distribution of data. <br><br>e.g., a model trained to predict house prices based on data from 2010 might perform poorly when predicting prices in 2020, due to changes in the housing market over time (domain shift). <br><br>Types of domain shift:<br>- Covariate Shift<br>- Concept Drift<br>- Prior Probability Shift|
| <a id="gradient"></a>Gradient | Measures of how much an output value of a function changes when you change the inputs a little bit. |
| Gradient Descent | Technique to change parameters of the NN ot make them "better". i.e., the mathematical function underneath to "learn" and do something useful. Often times, we try to minise the loss function (such as MAE). |
| Horizontal scaling | Also known as scaling out, is a method of adding more machines to a network to improve system performance and handle increased workload. This approach allows a system to serve more concurrent users by distributing the load across multiple servers or systems. | 
| Idiomatic Python | It refers to the writing of Python code in a way that is considered the most appropriate and efficient according to the standards and principles of Python. It's about using Python's constructs and data structures with maximum efficiency and readability. <br>For e.g., <br> - List comprehensions<br>- Using `with` for File Operations <br> - Using `enumerate` for iterating with indices. |
| Inference | Using trained model to get predictions |
| L1 norm | Also known as mean absolute error (<a id="mae"></a><b>MAE</b>).|
| L2 norm | Also known as root mean square error (<a id="rmse"></a><b>RMSE</b>). <br>MSE will penalise bigger mistakes more heavily than the MAE, and be more lenient with small mistakes. |
| Learning rate |  One of the most important hyper-parameter to set when training a NN. Often, this learning rate is multiplied with gradients of the parameters to update the parameters (such that the loss would be minimised). <br>Often a number netewen 0.001 and 0.1, although it could be anything|
| Learning rate finder | This is a method to find a good initial learning rate. The learning rate finder increases the learning rate after each batch and records the loss. It then plots the loss against the learning rate. The learning rate just before the loss starts to explode is usually a good initial learning rate. |
| Learning rate schedule (or decay) | Decrease learning rate over the epochs as we train to avoid overshooting of minimum point in the loss function due to a high learning rate.|
| Loss | | 
| Loss function | Return a value based on prediction and target, where lower values correspond to "better" predictions. |
| LSTM | Long short-term memory (widely used for speech recognition and other text modelling tasks) | 
| Model | Consists of two parts:<br>1. Architecture<br>2. Trained parameters |
| <a id="mse"></a> Mean squared error (MSE) | |
| Neural Network | Just a mathematical function, but a very expressive one that can approximate any c omputable function, given enough parameters. |
| Object detection | Recognizing where objects in an image are, and highlight their locations and name of the each found object. <br> Variants: <br> - [Segmentation](#segmentation)|
| Object recognition | Computers recognizing what items are in an image. |
| Optimizer step | Also known as stepping our parameters. It's the process of adjusting the parameters using the gradient and learning rate, usually as $w = w - gradient(w) \times \text{lr}$<br> Usually, we want to adjust the parameters in the direction of slope as our goal is to minimise the loss |
| Parameters | The values that are learnt by the NN model during training. |
| <a id="rank"></a><i>rank</i> | Number of dimensinos or axes in a tensor. Don't confuse rank with [shape](#shape) and [axis](#axis)/[dimensions](#dimensions). |
| Rectified Linear Unit (ReLU) | A combination of <br>- linear function (multiplying things together and adding up like $ax+b$) and <br> - simply replacing all negative numbers with zero (like `max(x,0)`)|
| <a id="segmentation"></a>Segmentation | A variant of object detection, where every pixel is categorised based on what kind of object it's part of. Useful for self-driving vision. |
| Stochasic Gradient Descent (SGD) | Try to <i>minimise</i> the loss. <br> For continuous data, it's common to use [MSE](#mse). |
| Out-of-domain data|  Very common problem in ML. <br>Refers to the data that falls outside the range of the training dataset. In other words, it's data that the model has not seen before during its training phase. There may be data that our model sees in production which is very different to what it saw during training.  <br>e.g., if you train a model to recognize images of cats and dogs, and then you give it an image of a car, the car image would be considered out-of-domain data. |
| <a id="shape"></a> <i>Shape</i> | Size of each axis of a tensor. |
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