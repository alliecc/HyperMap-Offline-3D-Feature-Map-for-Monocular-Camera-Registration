[Code coming soon]

# HyperMap:Offline 3D Feature Map for Monocular Camera Registration


<img src="https://github.com/alliecc/HyperMap-Offline-3D-Feature-Map-for-Monocular-Camera-Registration/blob/master/front_v4.png" class="center" height="200">

Accurate localization is essential for autonomous operationin many problem domains. This is most often performed by comparingLiDAR scans collected in real-time to a HD point cloud based map. Whilethis enables centimeter-level accuracy, it depends on an expensive LiDARsensor at run time. Recently, efforts have been underway to reduce costby using cheaper cameras to perform 2D-3D localization. In contrast to previous work that learns relative pose by comparing projected depthand camera images, we propose HyperMap, a paradigm shift from onlinedepth feature extraction to offline map feature computation for the 2D-3Dcamera registration task through end-to-end training.

We first perform offline 3D sparse convolution to extract and compressthe voxelwise hypercolumn features for the whole map. Then at run-time,we project and decode the compressed map features to the rough initialcamera pose to form a virtual feature image. A CNN is then used topredict the relative pose between the camera image and the virtual featureimage. In addition, we propose a novel differentiable occlusion handlinglayer, especially designed for large points clouds, to remove occludedpoints  in  projection.  Our  experiments  on  synthetic  and  real  datasetsshow that, by feature compression and shifting the feature computationload to offline process, we reduced map size by 27−53% and accelerateonline computation by 44−76% while maintaining comparable or betterperformance
