# GANs  
Contains all my GAN-related projects.</br></br>

## 1. Simple GAN  
<table>
  <tr>
    <th><h2>MNIST</h2></th>
    <th><h2>Simple GAN</h2></th>
  </tr>
  <tr>
    <td><img src="assests/Mnist.JPG" width="400"/></td>
    <td><img src="assests/SimpleGAN_Result.JPG" width="400"/></td>
  </tr>
</table>
<ul>
  <li>Basic GAN implementation where both the generator and discriminator use simple neural networks.</li>
</ul>

## 2. DCGAN  
<table>
  <tr>
    <th><h2>Fashion MNIST</h2></th>
    <th><h2>DCGAN</h2></th>
  </tr>
  <tr>
    <td><img src="assests/DCGAN_FashionMnist.png" width="400"/></td>
    <td><img src="assests/DCGAN_Result.png" width="400"/></td>
  </tr>
</table>
<ul>
  <li>A GAN implementation where the generator uses transposed convolutions (ConvTranspose2d) and the discriminator uses standard convolutions (Conv2d).</li>
  <li>According to the results, the model is unstable and experiences mode collapse, where the same class is always produced.</li>
</ul>
