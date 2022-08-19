# CryoRL-pytorch-data

Dataset ("Aldolase") used in https://github.com/IBM/CryoRL-pytorch and [Optimized path planning surpasses human efficiency in cryo-EM imaging](https://doi.org/10.1101/2022.06.17.496614).

The dataset consists of image files cropped and converted from original cryo-EM images in mrc format.

Note that our previous paper [CryoRL: Reinforcement Learning Enables Efficient Cryo-EM Data Collection](https://arxiv.org/abs/2204.07543) used a classifier instead of a regressor. The train-test split was slightly different as well.

## Data preparation description

Patch level images were converted from mrc to png format (8-bit) using e2proc2d.py.

With hole coordinates from Leginon database (obtained when collecting the systematic dataset as ground truth), individual hole images were cropped with boxes of 150x150 px.

The CTFMaxRes values were also obtained from Leginon database and matched with the corresponding hole images.
