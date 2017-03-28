# Paper

* **Title**: Deep Learning based Large Scale Visual Recommendation and Search for E-Commerce
* **Authors**: Devashish Shankar, Sujay Narumanchi, Ananya H A, Pramod Kompalli, Krishnendu Chaudhury
* **Link**: https://arxiv.org/abs/1612.08242
* **Tags**: Neural Network, Deep Ranking
* **Year**: 2017

# Summary

* What
  * They suggest a new model for image search on fashion based on deep ranking.

* How
  * Model: 
    * Triplet deep ranking (based on VGG-16)
    * Parrallel shallow convolution network layer (capture high, low details)
    * Visualization of the model:
      * ![Visnet Model](images/Visnet_model.png?raw=true "Visnet Model")
  * Suggest a mothod to create training data:
    * First using only catalogue to training
      * Using basic score technique to generate triplet 
        * alexnet Fc 7 layer
        * color Hist: histogram of image background
        * Pattern net
      * q, p, n:
        * p: random
        * p: top 200 image similar to q on same class
        * n: 500 - 1000 top image similar to q on same class or image random from other class (30% in, 70% out)
      * Human validate
    * Add Exact Street2Shop dataset created by Kiapour et al. in [14] to improve (M. Hadi Kiapour, Xufeng Han, Svetlana Lazebnik, Alexander C. Berg, and Tamara L. Berg. 2015. Where to Buy It: Matching Street Clothing Photos in Online Shops. In Proc. ICCV.)
    * Using image localization: using the Faster R-CNN (FRCNN) approach outlined in [24]  (Shaoqing Ren, Kaiming He, Ross Girshick, and Jian Sun. 2015. Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks. In Proc.NIPS.)