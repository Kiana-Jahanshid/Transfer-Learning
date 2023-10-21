# Recognition tasks 


# Description 

Here , i have used `InceptionResNetV2` architecture . <br />
we use pre-trained weights on `imagenet` dataset. <br />
we will assign `include_top=False` to remove the upper Fully-connected layers , then add a Flatten layer , and Dense layers . <br />
input_shape of this architecture must be (299,299,3) :
```
model = tf.keras.applications.InceptionResNetV2(weights="imagenet" , include_top=False , input_shape=(299,299,3)) 
```

we are going to have 3 recognition tasks , with 3 different below datasets :

1)   `7-7 faces` : contains 14 classes of men and women aligned faces  
2)   `5 naimals` : contains 5 classes of animals
3)   `17 flowers` : contains 17 classes of flowers


# How to install 
```
pip install -r requirements.txt 
```


# How to run 


You only need to Run `files.ipynb` . At the end of the code , in inference part , corresponding predicted labels are shown .  


# RESULTS 
Here is the loss and accuracy results : <br />
<br />
validation accuracy | 5-animals | 17-flowers | 7-7 faces
|:---: | :---: | :---: | :---: |
using Transfer learning | 0.9766  | 0.9355 | 0.88 | 
without Transfer learning | 0.7237 | 0.7692 | ___ | 

<br />
<br />


## confusion matrix and loss-acc diagram for face recognition :
<p float="center">
    <img src  = "assets/7-7 faces/conf_mat.png" width=400 /> 
    <img src  = "assets/7-7 faces/lossacc.png" width=350 /> 
</p>
<br />

## confusion matrix and loss-acc diagram for flowers recognition :
<p float="center">
    <img src  = "assets/17 flowers/conf_mat.png" width=400 /> 
    <img src  = "assets/17 flowers/loss-acc.png" width=350 /> 
</p>
<br />

## confusion matrix and loss-acc diagram for animals recognition :
<p float="center">
    <img src  = "assets/5 animals/conf_mat.png" width=400 /> 
    <img src  = "assets/5 animals/loss-acc.png" width=350 /> 
</p>