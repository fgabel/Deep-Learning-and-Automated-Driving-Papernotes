# DEEP LEARNING and AUTOMATED DRIVING > papernotes
personal notes and key points on papers related to DL and AD papers in under 400 words

## Section: Deep Learning

*01/ 2021*

- [Mixed Precision Training](https://arxiv.org/pdf/1710.03740.pdf) - [short summary](COMING SOON)
  - **TLDR**: Three techniques for neural network compression for faster inference and training speed: master copying FP32 weights, loss scaling and FP16 calculation/FP32 accumulation.

- [What Do Compressed Deep Neural Networks Forget?](https://arxiv.org/pdf/1911.05248v2.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/What%20Do%20Compressed%20Deep%20Neural%20Networks%20Forget%3F.md)
  - **TLDR**: Compression disproportionately impacts model performance on the underrepresented long-tail of the data distribution.

*12/ 2020*

- [Detection and Retrieval of Out-of-Distribution Objects in Semantic Segmentation](https://arxiv.org/pdf/2005.06831.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Detection%20and%20Retrieval%20of%20Out-of-Distribution%20Objects%20in%20Semantic%20Segmentation.md)
  - **TLDR**: Yet another interesting method for uncertainty quantification in semantic segmentation NNs.

- [Attribution Preservation in Network Compression for Reliable Network Interpretation](https://arxiv.org/pdf/2010.15054v1.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Attribution%20Preservation%20in%20Network%20Compression%20for%20Reliable%20Network%20Interpretation.md)
  - **TLDR**: Compressing neural networks for inference is in conflict with information attribution, which can be used for explanation of network outputs in safety-critical domains.

- [STDP-based spiking deep convolutional neural networks
for object recognition](https://arxiv.org/pdf/1611.01421.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/STDP-based%20spiking%20deep%20convolutional%20neural%20networks%20for%20object%20recognition.md)
  - **TLDR**: Unlike "classical" neural networks, bio-inspired spiking neural net make heavy use of timing for both learning and inference.
  
 *11/ 2020*

- [Towards spike-based machine intelligence with neuromorphic computing](https://www.nature.com/articles/s41586-019-1677-2) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Towards%20spike-based%20machine%20intelligence%20with%20neuromorphic%20computing.md)
  - **TLDR**: The brain has spiking neurons, current AI does not. Neuromorphic computing utilizes algorithms and software–hardware codesign to realize spiking neural networks.
  
 *09 / 2020*
- [The Fishyscapes Benchmark:
Measuring Blind Spots in Semantic Segmentation](https://arxiv.org/pdf/1904.03215.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/The%20Fishyscapes%20Benchmark:%20Measuring%20Blind%20Spots%20in%20Semantic%20Segmentation.md)
  - **TLDR**: A dataset and benchmark for the critical task of handling unknown objects in semantic segmentations.
 
 *08 / 2020*
- [Deep Compression: Compressing Deep Neural Networks with pruning, trained quantization and Huffman coding](https://arxiv.org/pdf/1510.00149.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Deep%20Compression:%20Compressing%20Deep%20Neural%20Networks%20with%20pruning,%20trained%20quantization%20and%20Huffman%20coding.md)
  - **TLDR**: One of the very first papers on modern neural network compression. Iconic. 
 
*07 / 2020*
- [Training End-to-End Analog Neural Networks with Equilibrium Propagation](https://arxiv.org/pdf/2006.01981.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Training%20End-to-End%20Analog%20Neural%20Networks%20with%20Equilibrium%20Propagation.md)
  - **TLDR**: A proof that end-to-end training of analog neural networks works in practice.

- [Disentangling Monocular 3D Object Detection
](http://openaccess.thecvf.com/content_ICCV_2019/papers/Simonelli_Disentangling_Monocular_3D_Object_Detection_ICCV_2019_paper.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Disentangling%20Monocular%203D%20Object%20Detection.md)
  - **TLDR**: Interesting. Deriving 3D bounding boxes from 2D images, powered by an improved loss function.

*05 / 2020*
- [EfficientDet: Scalable and Efficient Object Detection](https://arxiv.org/pdf/1911.09070.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/EfficientDet:%20Scalable%20and%20Efficient%20Object%20Detection.md)
  - **TLDR**: A clever architecture for multi-scale feature aggregation vastly improves the state of the art in object detection and semantic segmentation. Awesome.

*03 / 2020*
- [Class-Balanced Loss Based on Effective Number of Samples](https://vision.cornell.edu/se3/wp-content/uploads/2019/05/class_balanced.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Class-Balanced%20Loss%20Based%20on%20Effective%20Number%20of%20Samples.md)
  - **TLDR**: Vanilla reweighting or resampling strategies suck at representing long-tailed distributions. Geometrical representations of data can help with balancing labels for deep learning.

*02 / 2020*
- [MeteorNet: Deep Learning on Dynamic 3D Point Cloud Sequences](http://openaccess.thecvf.com/content_ICCV_2019/papers/Liu_MeteorNet_Deep_Learning_on_Dynamic_3D_Point_Cloud_Sequences_ICCV_2019_paper.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/MeteorNet:%20Deep%20Learning%20on%20Dynamic%203D%20Point%20Cloud%20Sequences.md)
  - **TLDR**: Incorporating spatiotemporal relationships by design improves performance. Based on PointNet.
- [Performance Evaluation of Object Tracking Algorithms](https://pdfs.semanticscholar.org/ad76/bdc7d06a7ec496ac788d667c6ad5fcc0fe41.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Performance%20Evaluation%20of%20Object%20Tracking%20Algorithms.md)
  - **TLDR**: Performance for video tracking algorithms can be evaluated with various metrices with different strengths and weaknesses.


*01 / 2020*
- [FuseSeg: LiDAR Point Cloud Segmentation Fusing Multi-Modal Data](https://arxiv.org/pdf/1912.08487.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/FuseSeg:%20LiDAR%20Point%20Cloud%20Segmentation%20Fusing%20Multi-Modal%20Data.md)
  - **TLDR**: Cool high-level sensor fusion method of RGB and LiDAR data using learned point correspondences.
- [StarNet: Targeted Computation for
Object Detection in Point Clouds](https://arxiv.org/pdf/1908.11069.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/StarNet:%20Targeted%20Computation%20for%20Object%20Detection%20in%20Point%20Clouds.md)
  - **TLDR**: Yet another method for non-volumetric 3D object detection. State-of-the-art on Waymo Open.

*12 / 2019*
- [PointRend: Image Segmentation as Rendering](https://arxiv.org/pdf/1912.08193.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/PointRend:%20Image%20Segmentation%20as%20Rendering.md)
  - **TLDR**: In semantic segmentation, focusing on areas of high uncertainty along with adaptively upsampling seems to be a winning combination.
- [PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation](https://arxiv.org/pdf/1612.00593.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/PointNet:%20Deep%20Learning%20on%20Point%20Sets%20for%203D%20Classification%20and%20Segmentation.md)
  - **TLDR**: Performing 3D semantic segmentation on unordered point sets without 3D convolutions.
- [Adversarial Examples Improve Image Recognition](https://arxiv.org/pdf/1911.09665.pdf) - [short summary](coming soon)
  - **TLDR**: Image classification is already at human level, but it can further be improved with adversarial examples.

*11 / 2019*

- [Rethinking Atrous Convolution for Semantic Image Segmentation (DeepLab)](https://arxiv.org/abs/1706.05587) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Rethinking%20Atrous%20Convolution%20for%20Semantic%20Image%20Segmentation.md)
  - **TLDR**: Atrous convolutions resolves the issue of intentional information loss through maxpooling. Also, control the field-of-view of filters more efficiently.
  
- [Gaussian YOLOv3: An Accurate and Fast Object Detector Using Localization
Uncertainty for Autonomous Driving](https://arxiv.org/pdf/1904.04620.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Gaussian%20YOLOv3:%20An%20Accurate%20and%20Fast%20Object%20Detector%20Using%20Localization%20Uncertainty%20for%20Autonomous%20Driving.md)
  - **TLDR**: Modelling the uncertainty in bounding box predictions of YOLOv3 as a Gaussian parameter.
  
*10 / 2019*

- [The ML Test Score: A Rubric for ML Production Readiness and Technical Debt Reduction](https://storage.googleapis.com/pub-tools-public-publication-data/pdf/aad9f93b86b7addfea4c419b9100c6cdd26cacea.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/The%20ML%20Test%20Score:%20A%20Rubric%20for%20ML%20Production%20Readiness%20and%20Technical%20Debt%20Reduction.md)
  - **TLDR**: Bringing software engineering best practices to deep learning.
  
- [VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection](https://arxiv.org/abs/1711.06396) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/VoxelNet:%20End-to-End%20Learning%20for%20Point%20Cloud%20Based%203D%20Object%20Detection.md)
  - **TLDR**: End-to-end deep learning on point clouds requires special operations, in this case Stacked Voxel Feature Encoding.

*09 / 2019*

- [A critique of pure learning: what artificial neural nets can learn from animal brains](https://www.biorxiv.org/content/biorxiv/early/2019/03/20/582643.full.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/A%20critique%20of%20pure%20learning:%20what%20artificial%20neural%20nets%20can%20learn%20from%20animal%20brains.md)

*08 / 2019*
- [Events-to-Video: Bringing Modern Computer Vision to Event Cameras](http://rpg.ifi.uzh.ch/docs/CVPR19_Rebecq.pdf) - [short summary](coming soon)
- [Fast Online Object Tracking and Segmentation: A Unifying Approach](https://arxiv.org/abs/1812.05050) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Fast%20Online%20Object%20Tracking%20and%20Segmentation:%20A%20Unifying%20Approach.md)
- [Hybrid Task Cascade for Instance Segmentation](https://arxiv.org/abs/1901.07518) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Hybrid%20Task%20Cascade%20for%20Instance%20Segmentation.md)

*07 / 2019*

- [LaserNet: An Efficient Probabilistic 3D Object Detector for Autonomous Driving](https://arxiv.org/abs/1903.08701) - [coming soon]()
- [A Survey of Deep Learning-based Object Detection](https://arxiv.org/pdf/1907.09408.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/A%20Survey%20of%20Deep%20Learning-based%20Object%20Detection.md)
  - **TLDR**: Great resource on 2D and 3D object detection and corresponding datasets.

*06 / 2019*

- [VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection](https://arxiv.org/pdf/1711.06396.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/VoxelNet:%20End-to-End%20Learning%20for%20Point%20Cloud%20Based%203D%20Object%20Detection.md)

- [Visualizing the Loss Landscape of Neural Nets](https://arxiv.org/abs/1712.09913) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Visualizing%20the%20Loss%20Landscape%20of%20Neural%20Nets.md)
  - **TLDR**: Neat method to learn about the shape of the loss surface in deep neural networks.

- [Weight Agnostic Neural Networks](https://arxiv.org/abs/1906.04358) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Weight%20Agnostic%20Neural%20Networks.md)
- [Adversarial Examples Are Not Bugs, They Are Features](https://arxiv.org/pdf/1905.02175v2.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Adversarial%20Examples%20Are%20Not%20Bugs%2C%20They%20Are%20Features.md)
  - **TLDR**: Dividing features of an image classifier into robust and non-robust helps causally determine effects of adversarial examples

*05 / 2019*

- [GAN Dissection: Visualizing and Understanding Generative Adversarial Networks](https://arxiv.org/abs/1811.10597) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/GAN%20Dissection:%20Visualizing%20and%20Understanding%20Generative%20Adversarial%20Networks.md)
- [Semantic Segmentation using Adversarial Networks](https://arxiv.org/pdf/1611.08408.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Semantic%20Segmentation%20using%20Adversarial%20Networks.md)


*04 / 2019*

- [Few-Shot Unsupervised Image-to-Image Translation](https://arxiv.org/abs/1905.01723) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Few-Shot%20Unsupervised%20Image-to-Image%20Translation.md)


*11 / 2018*

- [Large Scale GAN Training for High Fidelity Natural Image Synthesis](https://arxiv.org/pdf/1809.11096v1.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Large%20Scale%20GAN%20Training%20for%20High%20Fidelity%20Natural%20Image%20Synthesis.md)

*10 / 2018*

- [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://arxiv.org/abs/1810.04805) - [short summary]()
  - **TLDR**: Transformers are the designated successor of LSTMs and outperform them on many tasks.

*12 / 2017*

- [Dynamic Routing Between Capsules](https://arxiv.org/pdf/1710.09829.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Dynamic%20Routing%20Between%20Capsules.md)
  - **TLDR** Introducing a prior with regards to neuron grouping makes various learning tasks easier, but computationally challenging.
*11 / 2017*

- Video Object Segmentation with Re-identification
 [PDF](https://arxiv.org/pdf/1708.00197.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Video%20Object%20Segmentation%20with%20Re-identification)


*10 / 2017*

- [Learning Video Object Segmentation from Static Images](https://arxiv.org/pdf/1612.02646.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Learning%20Video%20Object%20Segmentation%20from%20Static%20Images.md)

*09 / 2017*

- [Training RNNs as Fast as CNNs](https://arxiv.org/pdf/1709.02755.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Training%20RNNs%20as%20Fast%20as%20CNNs.md)
**TLDR**: Temporal dependencies slow down RNN training. This can be remedied using highway connections.
- Video Frame Interpolation via Adaptive Separable Convolution [ARXIV](https://arxiv.org/abs/1708.01692) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Video%20Frame%20Interpolation%20via%20Adaptive%20Separable%20Convolution.md)
- Speech recognition with deep recurrent neural networks [ARXIV](https://arxiv.org/abs/1303.5778) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/speech-recognition-with-deep-recurrent-neural-networks.md)
- Brain Tumor Segmentation with Deep Neural Networks [ARXIV](https://arxiv.org/pdf/1505.03540.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Brain%20Tumor%20Segmentation%20with%20Deep%20Neural%20Networks.md)

## Section: Automated Driving

*12 / 2020*

- [Tire and Vehicle Dynamics](https://www.elsevier.com/books/tire-and-vehicle-dynamics/pacejka/978-0-08-097016-5) - [short summary](Coming soon.)
  - **TLDR**: Coming soon.

 *11/ 2020*
 - [Attribution Preservation in Network Compression for Reliable Network Interpretation](https://arxiv.org/pdf/2010.15054v1.pdf) - [short summary](TBD)
  - **TLDR**: Compressing neural networks for inference is in conflict with information attribution, which can be used for explanation of network outputs in safety-critical domains.

*01 / 2020*

- [Night-Time Vehicle Sensing in Far Infrared Image with Deep Learning](https://www.hindawi.com/journals/js/2016/3403451/) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Night-Time%20Vehicle%20Sensing%20in%20Far%20Infrared%20Image%20with%20Deep%20Learning.md)
  - **TLDR**: Far infrared automotive sensors offer night vision and can be used for learning-based object detection.
- [Next Generation Radar Sensors in Automotive
Sensor Fusion Systems](https://ieeexplore.ieee.org/document/8126389) - [short summary](soon)
  - **TLDR**: Radars are cool and provide unique sensoric capabilities indespensable for successful fully AD.


*12 / 2019*
- [Road detection based on the fusion of Lidar and image data](https://journals.sagepub.com/doi/full/10.1177/1729881417738102) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Road%20detection%20based%20on%20the%20fusion%20of%20Lidar%20and%20image%20data.md)
  - **TLDR**: Fuse image and 3D LiDaR data by first projecting the point clouds onto 2D monocular images, then perform road detection using a conditional random field.
- Certifiability of Deep Learning models in security critical industries such as automotive [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Certifiability%20of%20Deep%20Learning%20models%20in%20security%20critical%20industries%20such%20as%20automotive.md)
  - **TLDR**: Large-scale deployment of deep learning models needs certification from authorities, which does not exist yet.

*11 / 2019*

- [Stereo R-CNN based 3D Object Detection for Autonomous Driving](https://arxiv.org/pdf/1902.09738.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Rethinking%20Atrous%20Convolution%20for%20Semantic%20Image%20Segmentation.md)
  - **TLDR**: End-to-end learning of an 3D object detection model using stereo camera inputs.

*10 / 2019*

- [Autonomous Vehicle Implementation Prediction](https://www.vtpi.org/avip.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Autonomous%20Vehicle%20Implementation%20Predictions.md)
  - **TLDR**: Autonomous cars might cause enormous benefits to society, but we're not there yet. From an city planning perspective.
  
*08 / 2019*

- [DynaNet: Neural Kalman Dynamical Model for Motion Estimation and Prediction](https://arxiv.org/pdf/1908.03918.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Deep%20Sensor%20Fusion%20for%20Real-Time%20Odometry%20Estimation.md)
- [A Multimodal Vision Sensor for Autonomous Driving](https://arxiv.org/pdf/1908.05649.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Deep%20Sensor%20Fusion%20for%20Real-Time%20Odometry%20Estimation.md)
- [Deep Sensor Fusion for Real-Time Odometry Estimation](https://arxiv.org/pdf/1908.00524.pdf) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Deep%20Sensor%20Fusion%20for%20Real-Time%20Odometry%20Estimation.md)
  - **TLDR**: Theoretically, self-localization can be enhanced considerably using 2D LiDAR-scanners. The practicability of the approach is to be questionned.


*07 / 2019*

- [ChauffeurNet: Learning to Drive by Imitating the Best and Synthesizing the Worst](https://arxiv.org/abs/1812.03079) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/ChauffeurNet:%20Learning%20to%20Drive%20by%20Imitating%20the%20Best%20and%20Synthesizing%20the%20Worst.md)
  - **TLDR**: Imitation learning (what children do) can work for autonomous driving, but only if you provide data on malicious situations such as going off the road / collisions (e.g. via simulation).

*06 / 2019*

- [Self-Driving Cars: A Survey](https://arxiv.org/abs/1901.04407) - [short summary](https://github.com/fgabel/Deep-Learning-and-Automated-Driving-Papernotes/blob/master/comments/Self-Driving%20Cars:%20A%20Survey.md)
  - **TLDR**: Self-driving car architectures share many similar features. This paper gathers literature on all the subsystems necessary for it to run.

- [LaserNet: An Efficient Probabilistic 3D Object Detector for Autonomous Driving](https://arxiv.org/abs/1903.08701) - [short summary](coming soon)
