# Literature Review - Feature Matching

- **Reviewer's Name:** Madhava Pandiyan C N
- **Reference1:** [1] Yunpeng Li, Noah Snavely, Daniel P. Huttenlocher "Location Recognition using Prioritized Feature Matching" in ECCV 2010
- **Reference2:** [2] Szeliski, R. (2022). Feature detection and matching. Computer Vision: Algorithms and Applications (2nd ed.). Springer. https://szeliski.org/Book

## Useful Methodologies
### 1. Feature Descriptors
#### 1.1. SIFT Feature Descriptors
[2] SIFT (Scale invariant feature transform) features are formed by computing the gradient at pixel in a 16 x 16 window around the detected keypoint, using the appropriate level of the Gaussian pyramid at which the keypoint was detected. The 4 x 4 array of eight-bin histogram yields 128 non-negative values form a raw version of the SIFT descriptor vector.
Useful for finding feature correspondences between images. This feature correspondence can then be used by SfM to reconstruct 3D geometry.
Variant: 128-byte SIFT descriptor
#### 1.2. GIST Descriptor
Useful for retrieving similar images.
#### 1.3. PCA-SIFT
[2] It computes the x and y (gradient) derivatives over a 39 x 39 patch and then reduces the resulting 3042-dimentional vectorto 36using principal component analysis (PCA).
#### 1.4. SURF
[2] Another popular variant of SIFT is SURF, which uses box filters to approximate the derivatives and integrals used in SIFT.
#### 1.5. RootSIFT
[2] By simply re-normalizing SIFT descriptors using an L1 measure and then taking the square root of each component, a dramatic increase in performance (discriminability) can be obtained.
#### 1.6. GLOH
[2] Gradient location-orientation histogram (GLOH) is a variant of SIFT that uses a log-polar binning structure instead of the four quadrants.
#### 1.7. Steerable filter
[2] Steerable filters are combinations of derivative of Gaussian filters that permit the rapid computation of even and odd (symmetricand anti-symmetric) edge-like and corner-like features at all possible orientations. Because they use reasonably broad Gaussians, they too are somewhat insensitive to localization and orientation errors.

### 2. Others
#### 2.1. Visual Features
#### 2.2. Bag-of-words technique
Useful for retrieving similar images.
#### 2.3. SfM (Structure from Motion) technique
Useful for 3D reconstruction.
#### 2.4. Epitomes
#### 2.5. Clustering
Useful to derive specific images(/specific data) from a large collection of images(/data).

#### Image matching
Useful for 3D reconstruction.
#### Vocabulary tree
Used for proposing initial set of matchcing images for SIFT Feature Extractor.
#### Greedy Algorithm
This algorithm always selects the most valuable dataset or state.