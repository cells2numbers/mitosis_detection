# mitosis_detection

Notebook to create a training data set for mitosis detection. The sample data can be used to train a keras-rcnn network. 

## Data
A image series consisting of 399 phase contrast images with 552 mitotic events is used. The training data is available as template images where each mitotic cell is stored in an image with size 41x41. Each filename is "frame_x-coord_y-coord.png". 

For each mitosis, exactly one image is stored. In this script we use a template matching to extend the number of available training samples / data points: each mitotic event is identified in the frames before and after the recorded image. 

Using this method the number of samples is increased to 2902 samples. 


##  Training data for keras-rcnn 
To make the data **keras-rcnn ready** we create a list containg the bounding box for each mitosis. See
 https://github.com/broadinstitute/keras-rcnn

## The cetres data and mitosis data was published in 2011 and 2013. 


```
@article{rapoport2011novel,
  title={A novel validation algorithm allows for automated cell tracking and the extraction of biologically meaningful parameters},
  author={Rapoport, Daniel H and Becker, Tim and Mamlouk, Amir Madany and Schicktanz, Simone and Kruse, Charli},
  journal={PloS one},
  volume={6},
  number={11},
  pages={e27315},
  year={2011},
  publisher={Public Library of Science}
```

```
@inproceedings{becker2013combining,
  title={Combining phase contrast and immunofluorescence images using geometric hashing},
  author={Becker, Tim and Schultz, Sandra and Rapoport, Daniel H and Mamlouk, Amir Madany},
  booktitle={Biomedical Imaging (ISBI), 2013 IEEE 10th International Symposium on},
  pages={906--909},
  year={2013},
  organization={IEEE}
}
```

6.2017 TB
