## Data Annotation
Created a labelled Face Dataset using [VGG Annotator](http://www.robots.ox.ac.uk/~vgg/software/via/). The dataset contains the images of people looking in some direction which is Up, Down,Left,Right,Top, Back, UpRight, UpLeft, DownRight and DownLeft.

After Labelling, the centroid of bounding box with and without location is extracted and 4 potencial Anchor Boxes are generated using KMeans Algorithm.

rename_resize.py is the script to rename and resize the images to 400 x 400.

kmeans_with_location.py is used to find the potencial anchor boxes.

Here, I have calculated k means wth and and without including initial location.

[Link to Dataset](https://drive.google.com/open?id=1Qkj9p4t3rtqIyboWgeDqGQwe1OSIb80o)
