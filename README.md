# Neural Style transfer using VGG-16 CNN

### About

Implementation of <a href = "https://arxiv.org/abs/1508.06576"> A Neural Algorithm of Artistic Style </a> by <b> Leon A. Gatys, Alexander S. Ecker, Matthias Bethge </b> . This rendition has been done using a VGG-16 neural network. Keras and Tensorflow has been used along with Scipy <i>Fmin_l_bfgs_b optimizer</i>.

### Modifications

Instead of using a random noise initializer for the input image, the existing content image's values are copied to the input image. Styling weights are customizable depending upon the user specifications.

### Libraries

```bash
keras==2.3.1
tensorflow==1.15.3
scipy==1.4.1
```

### Algorithm

The styling, content and the output tensors are stacked up as the input image. This tensor passes into the VGG-16 and the output is also a <b>3xheightxwidthx3</b> tensor. The third tensor in the output layer (<i>Generated Image</i>) accounts for the smoothness. The activations in the <i>5th Convolutional block's <b>conv_2</b></i> is used to calculate content cost and various other convolutional layers belonging to each block is used to calculate style cost. Here , the regularization factor used for styling is primarily higher than the others. Image has been saved after deprocessing and reverting the effects brought by the VGG-16 passage.

### Running Instructions
To execute and run these files, download and open them in your Jupyter lab/ Jupyter notebook

If you do not have jupyter notebook/lab, download them using the following code :
```bash
pip install jupyterlab
```
```bash
pip install notebook
```
After installing , you may open your notebooks using the following command:

```bash
jupyter lab
```
```bash
jupyter notebook
```

### NOTE

<b> Please note that since my system couldn't handle any image size greater thatn 400x400x3 to pass into VGG, I have implemented this only for 128x196x3. If required, please set the image size to appropriate dimensions and train the network. </b>

### Contributors

<a href = "https://github.com/nickinack">Karthik Viswanathan</a>

