---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
Automating the process of fleece contaminant removal has the potential to drastically improve the quality of wool leaving the farm gate. Towards this goal, we present a method to automatically extract skirting lines, i.e., the separations between clean and contaminated wool of a fleece using RGB images. We propose a learning-based sparse-to-dense approach for estimating the non-rigid deformation of fleeces in order to estimate the skirting lines. Our method is bootstrapped from a set of sparse inlier feature correspondences, which are heavily filtered through a set of strict criteria. The inlier correspondences are then greedily expanded by adding correspondences from a denser set through a filtering process. This process is based on a learning approach that takes as inputs the pixel similarity and the consistency with their inlier neighbours. Each greedy iteration is initialized with a non-rigid deformation using as-rigid-as-possible.

![Rig used to collect dataset for experiment](dataset/wool_rig.jpg)

## Dataset

The dataset used to analyze the algorithm's performance consists of 24 pairs of images: one before and one after a sample of wool is skirted. The data is captured with the contaminant detection rig, where wool is placed on the roller table and observed by an overhead camera. A Balluff RGB camera is used with a resolution of 2464 × 1026 pixels.

First, an image is captured without markers. Then markers are placed on the unskirted wool and another image is captured. The wool is skirted with the markers on and a third image is captured. Finally, the markers are removed before the last image is captured.

To access the dataset used for this experiment, click [HERE](https://github.com/daniel-perezb/skirting_line/tree/main/dataset).

![Before Skirt Image](dataset/fleece00/00_00.png)

![After Skirt Image](dataset/fleece00/00_02.png)
