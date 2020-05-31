# sunglassesCNN
Sunglasses filter on a face (CNN/udacity/Computer Vision)

Facial Filters
Using trained CNN facial keypoint detector, you can now add filters to a person's face, automatically. 
<img src="/images/face_filter_ex.png" width=50% height=50%/>

#### Overlaying images

When we place this sunglasses image on top of another image, we can use the transparency channel as a filter.
If the pixels are non-transparent (alpha_channel > 0), overlay them on the new image.

#### Keypoint locations

In doing this, it's helpful to understand which keypoint belongs to the eyes, mouth, etc., so in the image below we also print the index of each facial keypoint directly on the image so you can tell which keypoints are for the eyes, eyebrows, etc.,

<img src="/images/landmarks_numbered.jpg" width=50% height=50%/>

It may be useful to use keypoints that correspond to the edges of the face to define the width of the sunglasses, and the locations of the eyes to define the placement.


# load in the train/test data
!mkdir /data
!wget -P /data/ https://s3.amazonaws.com/video.udacity-data.com/topher/2018/May/5aea1b91_train-test-data/train-test-data.zip
!unzip -n /data/train-test-data.zip -d /data