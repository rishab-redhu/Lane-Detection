# Lane-Detection
In this project, I use a deep learning-based approach to improve upon lane detection. My final model uses a fully convolutional neural network to output an image of a predicted lane.

## Training Data Stats
21,054 total images gathered from 12 videos (a mix of different times of day, weather, traffic, and road curvatures). 
17.4% were clear night driving, 16.4% were rainy morning driving, and 66.2% were cloudy afternoon driving. 
26.5% were straight or mostly straight roads, 30.2% were a mix or moderate curves, and 43.3% were very curvy roads. 
The roads also contain difficult areas such as construction and intersections. 
14,235 of the total that were usable of those gathered (mainly due to blurriness, hidden lines, etc.). 
1,420 total images originally extracted from those to account for time series (1 in every 10). 
227 of the 1,420 unusable due to the limits of the CV-based model used to label (down from 446 due to various improvements made to the original model) for a total of 1,193 images. 
Another 568 images (of 1,636 pulled in) gathered from more curvy lines to assist in gaining a wider distribution of labels (1 in every 5 from the more curved-lane videos; from 8,187 frames). 
In total, 1,761 original images. 
After checking histograms for each coefficient of each label for distribution, I created an additional 4,404 images using small rotations of the images outside the very center of the original distribution of images. This was done in three rounds of slowly moving outward from the center of the data (so those further out from the center of the distribution were done multiple times). 6,382 images existed at this point.
Finally, I added horizontal flips of each and every road image and its corresponding label, which doubled the total images. All in all, there were a total of 12,764 images for training. 

![1](https://user-images.githubusercontent.com/34485564/159104013-90daf40b-eef5-4841-9d49-2424900c3270.jpeg)

![2](https://user-images.githubusercontent.com/34485564/159104017-ca4b9d38-53d5-4729-bf5c-4f1b6e6717a1.jpeg)
![3](https://user-images.githubusercontent.com/34485564/159104020-dc9cb7d3-3ba9-4d45-8c49-9d5de99a7d61.jpeg)
![4](https://user-images.githubusercontent.com/34485564/159104024-e07a22bb-2c95-44b9-8159-dcf42125bf2c.jpeg)
