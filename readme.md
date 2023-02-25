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
      <li> Dice Score: 0.9043 </li>
      <li> Sensitivity: 0.9270 </li>
      <li> Specificity: 0.9803 </li>
     </ul>
     
  <br>
  <h2> Ghosted UNET Architecture </h2>
  <p> For Ghosted UNET Architecutre what we have done is ghosted basically the Convolution or Contraction Part and followed the same codebase for expansion part of the UNET </p>
  <p align='center'> <b> Note: </b> As it is still a work in progress I will be updating this log file as I reach more checkpoints in development cycle. </p>
</div>

