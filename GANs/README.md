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
  <li>A GAN using CNN where the generator upsamples (ConvTranspose2d) and the discriminator downsamples (Conv2d).</li>
  <li>The model is unstable and shows mode collapse, producing the same class repeatedly.</li>
</ul>

## 3. WGAN  
<table>
  <tr>
    <th><h2>Fashion MNIST</h2></th>
    <th><h2>WGAN</h2></th>
  </tr>
  <tr>
    <td><img src="assests/WGAN_FashionMnist.png" width="400"/></td>
    <td><img src="assests/WGAN_Result.png" width="400"/></td>
  </tr>
  <tr>
    <th><h2>WGAN-GP</h2></th>
    <th><h2>Conditional-WGAN-GP</h2></th>
  </tr>
  <tr>
    <td><img src="assests/WGAN_GP_Result.png" width="400"/></td>
    <td><img src="assests/Conditional_WGAN_GP_Result.png" width="400"/></td>
  </tr>
</table>

<ul>
  <li>Same as DCGAN, but uses Wasserstein loss instead which stabilizes training</li>
  <li>WGAN-GP use gradient penalty instead of weight cliping to penalize large weights.</li>
  <li>Conditional WGAN-GP guides generation with class labels, reducing mode collapse.</li>
  <li><strong>Note:</strong> Results may look worse than previous models because this was trained for only 25 epochs instead of 100.</li>
</ul>

## 4. Pix2Pix GAN  
<table>
  <tr>
    <th><h2>Input</h2></th>
    <th><h2>Result</h2></th>
    <th><h2>Ground Truth</h2></th>
  </tr>
  <tr>
    <td><img src="assests/Pix2PixGAN_Input_1.JPG" width="150"/></td>
    <td><img src="assests/Pix2PixGAN_Result_1.JPG" width="150"/></td>
    <td><img src="assests/Pix2PixGAN_Ground-Truth_1.JPG" width="150"/></td>
  </tr>
  <tr>
    <td><img src="assests/Pix2PixGAN_Input_2.png" width="150"/></td>
    <td><img src="assests/Pix2PixGAN_Result_2.png" width="150"/></td>
    <td><img src="assests/Pix2PixGAN_Ground-Truth_2.png" width="150"/></td>
  </tr>
</table>

<ul>
  <li>Generator: U-Net for mapping input to output images.</li>
  <li>Discriminator: PatchGAN that classify each image patch instead of the whole image.</li>
  <li>Loss: Adversarial (realism) + L1 (structural similarity).</li>
</ul>

## 5. Cycle GAN  
<table>
  <tr>
    <th><h2>Input Winter</h2></th>
    <th><h2>Result Summer</h2></th>
    <th><h2>Reconstructed Winter</h2></th>
  </tr>
  <tr>
    <td><img src="assests/Winter_Input.png" width="250"/></td>
    <td><img src="assests/Fake_Summer.png" width="250"/></td>
    <td><img src="assests/Winter_Reconstructed.png" width="250"/></td>
  </tr>
</table>

<table>
  <tr>
    <th><h2>Input Summer</h2></th>
    <th><h2>Result Winter</h2></th>
    <th><h2>Reconstructed Summer</h2></th>
  </tr>
  <tr>
    <td><img src="assests/Summer_Input.png" width="250"/></td>
    <td><img src="assests/Fake_Winter.png" width="250"/></td>
    <td><img src="assests/Summer_Reconstructed.png" width="250"/></td>
  </tr>
</table>

<ul>
  <li>Generator: 2 Generators consists of Downsampling → Residual Blocks → Upsampling</li>
  <li>Discriminator: 2 Discriminators consists of PatchGAN that classify each image patch instead of the whole image.</li>
  <li>Loss: Adversarial + Cycle (Reversible) + identity (Preserve)</li>
</ul>
