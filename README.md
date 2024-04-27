# MRE-462-SLAM
My SLAM Project for MRE 462
This is my submission for the SLAM project in MRE 462, taught by Mingshao Zhang. 

  The example provided first downloads the dataset that will be used throughout the process and puts it into a temporary file if said file does not already exist. It then inspects the dataset and creates a datastore of all the images to be referenced at any time. Then it looks at the first image and displays it to the user before specifying the characteristics of the camera used including focal length and the size of the image. After this, it specifies some more characteristics before going into the map initialization loop.

  The map initialization loop reads the current frame and compares it to later ones to see if enough matches can be made between them. It repeats this with each frame until it finds enough matches between them or is able to stretch them enough to find enough inlier points. If the program is able to initialize the map, it will tell the user which frames were used. Otherwise, it will show an error statement saying that it is unable to initialize it.

  The next section stores key frames according to specific map points. It looks at the frames found in the previous section and finds the connections between the two. It then uses information gathered in previous sections to add 3D map points as well as some of their characteristics and shows the correspondences in each frame.

  It then begins a section that tries to recognize where it is in the space and adjusts some aspects of it as needed such as the depth, pose, and points measured. After this, it starts plotting its estimated position, orientation, and key points on a 3D graph. It then captures each view it has and makes its way into the "Main Loop".

  
