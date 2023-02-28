<h1 align='center'> Unet_vs_Ghosted_Unet </h1>

<div>
  <p align='left'> The idea behind this repo is to create an Enviorment to observe how Unet segmentation will compare against a Unet_vs_Ghosted_Unet architecture for the work of 
    image segmentation </p>
    <p> So Far we have Completed UNET segmentation task. Currently Working on Ghosted UNET system after its been completed we are going to compare the number of parameters features geenrated and how it stacks up against the Original Unet model.</p>
    <h2> UNET Architecture </h3>
    <img src='https://miro.medium.com/max/1200/1*f7YOaE4TWubwaFF7Z1fzNw.png'>
    <p> Our UNET Model has 5 encoder and 4 decoder </p>
    <p> The number of features used are: </p>
    <ul>
      <li> 16 features </li>
      <li> 32 features </li>
      <li> 64 features </li>
      <li> 128 features </li>
      <li> 256 features </li>
    </ul>
  <p> Similarly The number of Parameters for the UNET Model is calculated to be: </p>
  
  
    Total params: 1,941,105
    Trainable params: 1,941,105
    Non-trainable params: 0
  
  <p> In the latest experiment Trained for 25 epochs we have obtained following scores for this model </p>
    <ul>
      <li> Dice Score: 0.8955  </li>
      <li> Sensitivity: 0.9095 </li>
      <li> Specificity: 0.9890 </li>
     </ul>
   <p> The Performance During Inference was observed as: </p>
   <ul>
     <li> Original Image: <br> <img src='https://user-images.githubusercontent.com/80937266/221606061-b7dfe1af-5ff6-4062-b7b2-da2c2002b703.jpg'></li>
     <li> Predicted Mask: <br> <img src='https://user-images.githubusercontent.com/80937266/221606501-30a5d4a0-bfc1-4116-a752-7d257928d3ee.jpg'></li>
  </ul>

  <br>
  <h2> Ghosted UNET Architecture </h2>
  <p> For Ghosted UNET Architecutre what we have done is ghosted basically the Convolution or Contraction Part and followed the same codebase for expansion part of the UNET </p>
  <p> After ghosting the same UNET structure had increased number of features for each contraction layer and parameters overall was observed to be drasitcally small for such large network with such large number of features. The final update is shown below: </p>
  <ul>
    <li> First Layer UNET Input Features: 16, Ghosted UNET Features: 20 </li>
    <li> First Layer UNET Input Features: 16, Ghosted UNET Features: 20 </li>
    <li> Second Layer UNET Input Features: 32, Ghosted UNET Features: 42 </li>
    <li> Second Layer UNET Input Features: 32, Ghosted UNET Features: 42 </li>
    <li> Third Layer UNET Input Features: 64, Ghosted UNET Features: 84 </li>
    <li> Third Layer UNET Input Features: 64, Ghosted UNET Features: 84 </li>
    <li> Forth Layer UNET Input Features: 128, Ghosted UNET Features: 166 </li>
    <li> Forth Layer UNET Input Features: 128, Ghosted UNET Features: 166</li>
    <li> Fifth Layer UNET Input Features: 256, Ghosted UNET Features: 332</li>
    <li> Fifth Layer UNET Input Features: 256, Ghosted UNET Features: 332</li>
  </ul>
  
  <p> Parameters for same UNET architecture with increased feature was obtained to be: </p>
  
      Total params: 1,828,063
      Trainable params: 1,828,063
      Non-trainable params: 0
    
  <p> From the above parameters for Ghosted UNET and Original UNET we can observe that there is a drastic difference of 113,042 parameters despite almost having 2    times the features </p>
  <p> In the latest experiment Trained for 20 epochs we have obtained following scores for this model </p>
    <ul>
      <li> Dice Score: 0.8824  </li>
      <li> Sensitivity: 0.9138  </li>
      <li> Specificity: 0.9776 </li>
     </ul>
   <p> The Performance During Inference was observed as: </p>
   <ul>
     <li> Original Image: <br> <img src='https://user-images.githubusercontent.com/80937266/221848259-124a519a-f4fc-43af-a1d0-6b83189dbb2c.png'></li>
     <li> Predicted Mask: <br> <img src='https://user-images.githubusercontent.com/80937266/221848471-bfa769fc-a0d5-45c8-bc1d-1a55ad9d684c.png'></li>
  </ul>
  <p align='center'> <b> Note: </b> As it is still a work in progress I will be updating this log file as I reach more checkpoints in development cycle. </p>
</div>



