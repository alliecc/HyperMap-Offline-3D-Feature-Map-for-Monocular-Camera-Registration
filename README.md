[update] ICRA 2021 paper link: https://www.cs.cmu.edu/~kaess/pub/Chang21icra.pdf

# HyperMap:Offline 3D Feature Map for Monocular Camera Registration

Ming-Fang Chang, Joshua Mangelson, Michael Kaess, Simon Lucey

See our video here: <a href="https://www.youtube.com/watch?v=CQsmS8RDsCE&feature=youtu.be">link</a>

<img src="https://github.com/alliecc/HyperMap-Offline-3D-Feature-Map-for-Monocular-Camera-Registration/blob/master/front_v4.png"  width="700" class="center">


# Motivation

Accurate localization is essential for autonomous operationin many problem domains. This is most often performed by comparing LiDAR scans collected in real-time to a HD point cloud based map. While this enables centimeter-level accuracy, it depends on an expensive LiDAR sensor at run time. Recently, efforts have been underway to reduce cost by using cheaper cameras to perform 2D-3D localization. In contrast to previous work that learns relative pose by comparing projected depthand camera images, we propose HyperMap, a paradigm shift from online depth feature extraction to offline map feature computation for the 2D-3D camera registration task through end-to-end training.

# System Structure


<img src="https://github.com/alliecc/HyperMap-Offline-3D-Feature-Map-for-Monocular-Camera-Registration/blob/master/network.png"  width="700" class="center">


We first perform offline 3D sparse convolution to extract and compress the voxelwise hypercolumn features for the whole map. Then at run-time, we project and decode the compressed map features to the rough initial camera pose to form a virtual feature image. A CNN is then used to predict the relative pose between the camera image and the virtual feature image. In addition, we propose a novel differentiable occlusion handlinglayer, especially designed for large points clouds, to remove occluded points  in  projection.  Our experiments  on synthetic and real datasets show that, by feature compression and shifting the feature computationload to offline process, we reduced map size by 27−53% and accelerate online computation by 44−76% while maintaining comparable or better performance

---------------------------------------------------------------------------------
This work was supported by the CMU Argo AI Center for Autonomous Vehicle Research
