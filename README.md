# ComfyUI on Amazon SageMaker AI Studio

**Author:** Hyunsoo Kim, Senior GenAI Specialist SA at AWS

This repository provides a guide for installing and running ComfyUI on Amazon SageMaker AI Studio.

## Table of Contents
1. [SageMaker AI Studio Environment Setup](#step-1-amazon-sagemaker-ai-studio-environment-setup)
2. [ComfyUI Installation and Environment Configuration](#step-2-comfyui-installation-and-environment-configuration-in-jupyterlab-space)
3. [ComfyUI Startup and Access](#step-3-comfyui-startup-and-access)
4. [Loading ComfyUI Workflow and Initial GUI Setup](#step-4-loading-comfyui-workflow-and-initial-gui-setup)
5. [Running ComfyUI Workflow](#step-5-running-comfyui-workflow)
6. [Viewing Result Images](#step-6-viewing-result-images)
7. [Additional Workflow Explanation](#step-7-additional-workflow-explanation)

## Step 1. Amazon SageMaker AI Studio Environment Setup
Access the AWS Management Console, select SageMaker AI --> SageMaker Studio.
In the SageMaker Studio console, create a JupyterLab space as shown in the figure below.
* You must select a GPU-enabled instance to run image generation models. (Recommended: ml.g5.2xlarge)
* Ensure sufficient storage to download and use multiple models. (Approximately 100GB)
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/1.png" />

## Step 2. ComfyUI Installation and Environment Configuration in JupyterLab Space
Click "Open JupyterLab" in the SageMaker Studio console as shown in the figure below to open the workspace.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/2.png" />

Clone the GitHub repository code files into the space as shown in the figure below.
Enter the following address in the Git Repositories URL:
https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI.git
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/3.png" />

Select ComfyUI_ModelPrep.ipynb from the cloned code files.
Select the correct kernel in the upper right corner, then run all cells automatically.
This file installs ComfyUI and configures the environment, then downloads essential AI models.
Proceed to the next step only after all cells have completed execution.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/4.png" />
* Download the "/workflow_temp" and "/input_img" folders from the cloned project folder to your local computer.
* "/workflow_temp" contains pre-written ComfyUI workflow examples, and "/input_img" contains image files for use in the workflow examples.

## Step 3. ComfyUI Startup and Access
Next, select ComfyUI_Start.ipynb.
Select the correct kernel in the upper right corner, then run all cells automatically.
This will run ComfyUI in the background.
https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI.git
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/5.png" />

When the following message appears on the Jupyter notebook screen, you can access ComfyUI.
Check the address bar of the web browser currently using JupyterLab.
It should look similar to the following:
https://<studio-id>.studio.<region>.sagemaker.aws/jupyter/default/lab
Extract the base URL. Copy the front part of the above address excluding the /lab part, then add /proxy/8188/ at the end and enter it in the web browser's address bar.
https://<studio-id>.studio.<region>.sagemaker.aws/jupyter/default/proxy/8188/
* Don't forget that the '/' symbol must be included at the very end of the above URL.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/6.png" />

## Step 4. Loading ComfyUI Workflow and Initial GUI Setup
When you access ComfyUI through the web browser, the following initial screen appears.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/7.png" />

Click "Workflow" in the top menu bar, then click "Open" to load the pre-shared workflow file.
* Select a workflow file from the "/workflow_temp" folder downloaded to your local computer.
* In this example, the item_with_bg_beta.json file was selected.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/8.png" />
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/9.png" />

When you load the workflow, notifications about uninstalled nodes will appear as shown in the figure below.
ComfyUI-IPAdapter_plus
WAS Node Suite (Revised)
ComfyUI's ControlNet Auxiliary Preprocessors
Open ComfyUI Manager and install all three node packs mentioned above.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/10.png" />
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/11.png" />

Once all node packs are installed, a restart button will appear at the bottom.
Click the restart button to restart ComfyUI.
Then reconnect through the address bar.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/12.png" />

Reconnect through the address bar.
You can confirm that the workflow has been properly loaded in the ComfyUI GUI screen.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/13.png" />

## Step 5. Running ComfyUI Workflow
Input the product image, composition sketch image, and style image in order through the three image loader nodes on the left.
Then click the execute button at the bottom to run the workflow.
You can view the generated images through the image preview node on the right in execution order.
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/14.png" />

## Step 6. Viewing Result Images
<table>
  <tr>
    <td>
      <img src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/ComfyUI_temp_fdtnx_00003_.png"" /><br/>
      Original Product Image
    </td>
    <td>
      <img src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/ComfyUI_temp_jnkxy_00005_.png" /><br/>
      Background Generation Draft Image
    </td>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/ComfyUI_temp_ijgfb_00005_.png" /><br/>
      First Refinement Image
    </td>
    <td>
      <img src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/ComfyUI_temp_geayj_00005_.png" /><br/>
      Second Refinement Image
    </td>
  </tr>
</table>

Second refinement image upscaled 4x
<img width="4418" height="1998" alt="1" src="https://github.com/Hyunsoo0128/comfyui_on_SageMakerAI/blob/main/img/ComfyUI_temp_tdmpe_00005_.png" />

## Step 7. Additional Workflow Explanation
### Purpose: AI-Based Automated Product Image Generation
This ComfyUI workflow is designed to generate professional, high-resolution product promotional images using three input images (product, composition, style).
It maximizes work efficiency by automating complex background generation and composition.

### Key Features
* Multi-ControlNet Control: Uses depth and canny maps simultaneously to precisely control the product's three-dimensionality and overall composition.
* Style Transfer via IPAdapter: Perfectly applies the style (lighting, color tone, texture) of a specific interior space image to the generated background.
* Background Generation using Inpainting: Generates new images only in the background area excluding the product image, achieving natural composition.
* Multi-stage KSampler Refinement: Progressively improves image detail and completeness through multiple KSampler stages.
* High-Resolution Upscaling: Provides high-quality images suitable for commercial use by 4x upscaling the final result.

### Detailed Workflow Description
This workflow consists of four main stages: Input & Preprocessing, Primary Background Generation, Secondary-Tertiary Refinement, and Final Upscaling.

#### 1. Input & Preprocessing
1.1. Product Image:
Background is automatically removed through the Image Rembg node.
Depth map is extracted with DepthAnythingPreprocessor to maintain the product's 3D form.

1.2. Composition Map Image:
A simple composition image with XYZ axis sketches.
Edge extraction through CannyEdgePreprocessor is used to control the overall structure of spaces like floors and walls.

1.3. Style Image:
An interior space photo with the desired atmosphere.
This image is directly input to the IPAdapterAdvanced node to determine the style of the generated background.

#### 2. Primary Background Generation (Pass 1: Background Generation via Inpainting)
2.1. A mask is generated from the product image with background removed, then inverted to select only the background area.
2.2. The VAEEncodeForInpaint node leaves only the background area empty in the Latent space based on this mask.
2.3. KSampler generates images by filling the empty background area with all conditions from ControlNet (Depth, Canny) and IPAdapter (Style) applied.
The result of this stage is the first image where product and background are combined.

#### 3. Secondary & Tertiary Refinement (Pass 2 & 3: Refinement)
3.1. Additional KSampler with IPAdapter:
The generated draft image is converted back to Latent, then resampled with a low denoise value (e.g., 0.4).
During this process, the product and background blend more naturally under the influence of IPAdapter and ControlNet, and the style is enhanced.
3.2. Additional KSampler without IPAdapter:
The first refinement result is converted back to Latent and final sampling is performed with an even lower denoise value (e.g., 0.2).
This stage uses the base model without IPAdapter influence to organize overall image details and improve completeness.

#### 4. Final Upscaling
The image after all refinement processes is passed to the ImageUpscaleWithModel node.
The final result is converted to high resolution using upscaling models like 4x-UltraSharp.
