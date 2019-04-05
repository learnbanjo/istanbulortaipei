X433-7 Machine Learning with Tensorflow Project

Title: Istanbul or Taipei?

Members: Aslihan Demirkaya & Shih-Chieh (Jerry) Hsu

Project Goal:
    Develop and train a system that can identify if the picture is taken in Istanbul or Taipei

Overview:
    Project consist of two major modules:
        1) Flicker Downloader
        2) Image Classifier

    Flickr Downloader:
        Using Flickr API to download Istanbul and Taipei pictures from Flickr
        Scale down and save to folders accordingly

    Image Classifier:
        Tensoflor Keras high level API allows one to build graphs with pre-built layers and modules.
        In this project, we use MobileNet module and 'softmax' layer to build the model
        Using Flickr pictures to train and validate the model we built


Platform:
    - Mac OS HighSierra on Macbook Pro
    - Jupyter Notebook 5.7.2
    - Python 3.6

Packages:
    - Pillow(PIL) 5.4.1
    - matplotlib 3.0.2
    - numpy 1.16.1
    - tensorboard 1.12.2
    - tensorflow 1.12.0
    - flickrapi 2.4.0
    - panda 0.3.1

External Resources:
    - MobileNet_V2 on Tensorflow Hub: https://tfhub.dev/google/imagenet/mobilenet_v2_100_224/feature_vector/2"
    - Flickr API: https://stuvel.eu/flickrapi-doc/

Execution Sequences:
    0) place demirkaya_hsu_project.ipynb, tensorboard_notebook2.py and istanbul_taipei folder in the same execution folder
    1) launch demirkaya_hsu_project.ipynb from Jupyter Notebook
    2) Images are included in the release package, but if you'd like to download images again,
       follow the following instruction

       a) Change redownload=False to redownload=True

       b) Change the following according to the downloading city
            keyword =  'istanbul' #'taipei'

       c) comment/uncomment the following code according to the downloading city

            pickle.dump(urls, open("istanbul_urls_flickr.pckl", 'wb'))
            !mkdir istanbul

            #pickle.dump(urls, open("taipei_urls_flickr.pckl", 'wb'))
            #!mkdir taipei

       Run code in the "Preparing the Data Set:" section to download pictures

       It takes about two hours to download pictures for each city.
       When running code in the "Preparing the Data Set:" section, make following changes accordingly


    3) With images available, run code in the "Image Classification using Tensorflow Hub with Keras"
       section sequentially.

       Some steps, such as training and validation, can take several minutes to complete