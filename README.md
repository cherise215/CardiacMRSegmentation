# CardiacMRSegmentation

[Paper](https://arxiv.org/abs/1907.01268)
Improving the generalizability of convolutional neural network-based segmentation on CMR images <br>
In arXiv 2019.

Code is available at https://gitlab.doc.ic.ac.uk/cc215/Cardiac_Multi_view_segmentation

# Performance on intra-domain and out-of-domain public datasets
- Our model trained on UKBB (~4000 training subjects), with extensive data augmentations (described in [1]) can achieve satisfactory performance on *unseen* out-of-domain public datasets, including [ACDC](https://www.creatis.insa-lyon.fr/Challenge/acdc/databases.html), [M&Ms](https://www.ub.edu/mnms/). We report the segmentation performance on these datasets in terms of Dice score below.

|                                                                          | UKBB test (600 subjects, 1200 frames: ED+ES) |        |        | ACDC (100 subjects, 200 frames: ED+ES) (unseen domain)|        |        | M&Ms (150 subjects, 300 frames: ED+ES) (unseen domain)   |        |        |
| ------------------------------------------------------------------------ | :------------------------------------------: | :----: | :----: | :------------------------------------: | :----: | :----: | :------------------------------------: | :----: | :----: |
| configurations                                                           |                      LV                      |  MYO   |   RV   |                   LV                   |  MYO   |   RV   |                   LV                   |  MYO   |   RV   |
| batch_size = 1, roi size = 256, z_score                                  |                    0.9383                    | 0.8780 | 0.8979 |                 0.8940                 | 0.8034 | 0.8237 |                 0.8862                 | 0.7889 | 0.8168 |

# Adversarially trained model performance on intra-domain and out-of-domain public datasets 
- We further enhance our model performance by applying our recent proposed adversarial data augmentation [2,3].

|               | UKBB   |        |        | ACDC (unseen domain)   |        |        | M&Ms  (unseen domain)    |        |        |
| ------------- | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
|               | LV     | MYO    | RV     | LV     | MYO    | RV     | LV     | MYO    | RV     |
| w/o Adv chain | 0.9383 | 0.8780 | 0.8979 | 0.8940 | 0.8034 | 0.8237 | 0.8862 | 0.7889 | 0.8168 |
| w/ Adv chain  | 0.9360 | 0.8732 | 0.8965 | 0.9060 | 0.8087 | 0.8404 | 0.8929 | 0.7987 | 0.8245 |

Please cite our work if you find this code useful.
--------------------------------------------------

[1] Chen, C. et al. (2020) ‘Improving the Generalizability of Convolutional Neural Network-Based Segmentation on CMR Images’, Frontiers in cardiovascular medicine, 7, p. 105. doi:10.3389/fcvm.2020.00105.

[2] Chen, C, et al. (2020). “Realistic Adversarial Data Augmentation for MR Image Segmentation.” In Medical Image Computing and Computer Assisted Intervention – MICCAI 2020, 667–77. Springer International Publishing.

[3] Chen, C, et al. "Enhancing MR Image Segmentation with Realistic Adversarial Data Augmentation." arXiv preprint arXiv:2108.03429 (2021).

--------------------------------------------------

@ARTICLE{Chen2020-gz,

  title         = "Improving the Generalizability of Convolutional Neural
                   {Network-Based} Segmentation on {CMR} Images",
       
  author        = "Chen, Chen and Bai, Wenjia and Davies, Rhodri H and Bhuva,
                   Anish N and Manisty, Charlotte H and Augusto, Joao B and
                   Moon, James C and Aung, Nay and Lee, Aaron M and Sanghvi,
                   Mihir M and Fung, Kenneth and Paiva, Jose Miguel and
                   Petersen, Steffen E and Lukaschuk, Elena and Piechnik,
                   Stefan K and Neubauer, Stefan and Rueckert, Daniel",
                   
  journal       = "Front Cardiovasc Med",
  
  pages         = "105",
  
  month         =  jun,
  
  year          =  2020,
  
  
}

@INPROCEEDINGS{Chen2020-ne,

  title     = "Realistic Adversarial Data Augmentation for {MR} Image
               Segmentation",
               
  booktitle = "Medical Image Computing and Computer Assisted Intervention --
               {MICCAI} 2020",
               
  author    = "Chen, Chen and Qin, Chen and Qiu, Huaqi and Ouyang, Cheng and
               Wang, Shuo and Chen, Liang and Tarroni, Giacomo and Bai, Wenjia
               and Rueckert, Daniel",
               
  publisher = "Springer International Publishing",
  
  pages     = "667--677",
  
  year      =  2020
  
}


