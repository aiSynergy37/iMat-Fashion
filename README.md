Dataset Details
Apparel instance segmentations include 27 main apparel objects (jackets, dresses, skirts, etc) and 19 apparel parts (sleeves, collars, etc). A total of 92 fine-grained attributes was annotated by expert for main apparel objects.
In this dataset, you are provided a large number of images and corresponding fashion/apparel segmentations. Images are named with a unique ImageId. You must segment and classify the images in the test set.

All of the test set images have fine-grained segmentations. The training set contains images both with and without fine-grained class segmentations.

This dataset contains images of people wearing a variety of clothing types in a variety of poses. It may have content that some consider sensitive. 


Dataset: https://www.datasetlist.com/


DATA preprocessing--deleted objects with an area of less than 20 pixels.applied light augmentatios from the albumentations library to the original image. Then I use multi-scale training: in each iteration, the scale of short edge is randomly sampled
from [600, 1200], and the scale of long edge is fixed as 1900.

Training details:
pre-train from COCO
optimizer: SGD(lr=0.03, momentum=0.9, weight_decay=0.0001)
batch_size: 16 = 2 images per gpu 