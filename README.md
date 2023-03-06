# Avanade-International-Women-s-Day-Hackathon
Avanade International Women's Day Hackathon - #EmbracingEquity this International Women's Day

# Test 

[ClicK to test the ML project](https://ml.azure.com/experiments/id/e34be1b0-38d6-4026-9370-47d902a60a4a/runs/7189338a-dbf9-408b-ab49-aa558e0139e7?wsid=/subscriptions/63ef8b26-b9c5-487a-9543-8bd28f703592/resourcegroups/Hacktech/providers/Microsoft.MachineLearningServices/workspaces/Hacktech&tid=f6365406-ec6d-449c-a9a1-95f6a70d355d&nsq=runStatus+in+{Completed}#/?graphId=808b800e-47a8-4f71-8845-b5944b16953f&label=carbon+prediction&newGraphId=808b800e-47a8-4f71-8845-b5944b16953f&path=%2Fexperiments%2Fid%2Fe34be1b0-38d6-4026-9370-47d902a60a4a%2Fruns%2F7189338a-dbf9-408b-ab49-aa558e0139e7&runId=7189338a-dbf9-408b-ab49-aa558e0139e7)
  
<br>
  
[Swagger Json](https://eastus2.api.azureml.ms/pipelines/swagger/pipelineendpointsubmit/swagger.json)
  
<br>

## Problem

![2](https://user-images.githubusercontent.com/101945531/222964587-ad6d4324-9141-4ddf-8116-14edde1facd6.png)
<br>
## Solution

![3](https://user-images.githubusercontent.com/101945531/222964635-aa46c568-2484-4517-94d5-272db06468f8.png)
<br>
## Create an Azure Machine Learning workspace
<li> Sign in to Azure Portal and select Create a resource.
<li> Search for Machine Learning and then click Create to start
<li> Configure the new Machine Learning resource.Select subscription, resource group, workspace name, region and click Review-Create.
<li> Wait for the workspace to be created (it may take several minutes) and then select Go to resource
<li> Click on Studio Web URL to go to your Azure Machine Learning workspace.
<br>
  
## workspace

<li> Create dataset->select Asset and then select Data + Create Dataset > 
  
![image](https://user-images.githubusercontent.com/101945531/223024145-6a92b181-cd78-4798-8bb5-de9cfcec1012.png)

  
<li> Provide relevant name and details  
  
![image](https://user-images.githubusercontent.com/101945531/223024294-98f5f5ef-bf6b-400d-a573-4bbcecb95801.png)

<li> In Datastore and file selection select Browse and choose the file on your local computer
  
![image](https://user-images.githubusercontent.com/101945531/223024355-8d48a658-33eb-4b2b-a105-8e3d2923fd38.png)


<li>Select database type where your data result needs to be stored
  
![image](https://user-images.githubusercontent.com/101945531/223024395-1a425506-f3cd-4a93-ac8a-239dd3b9bd2b.png)

  
<li>Upload data from local machine U CAN CHOOSE OTHER RESOURCES LIKE COSMODB,BLOB, ONLINE SERVICES ENDPOINT)

![image](https://user-images.githubusercontent.com/101945531/223024455-a70f8bb9-9d2e-442c-bc1a-36a9030089c7.png)

<li>Customize data parameter 
  
![image](https://user-images.githubusercontent.com/101945531/223024542-69d8cc3d-3587-4d87-918b-497c2db34cec.png)
  
<li>Change the schema type as per data type
  
![image](https://user-images.githubusercontent.com/101945531/223024599-5ec819ca-f6e2-425b-b3c2-16bb0eba5f71.png)
 
<li>Review and Create
  
![image](https://user-images.githubusercontent.com/101945531/223024646-7272c988-0c28-4b28-bfcb-6cd4d9cb9649.png)


## Create a new pipeline

<li> Select Designer and then select the plus sign (+) to create a new pipeline
  
 ![image](https://user-images.githubusercontent.com/101945531/222965580-6211f315-e9bc-4af2-8267-9fa1e6752420.png)

<li> Expand the Datasets section, select the dataset Removing gender bias in hiring through Azure AI's machine learning algorithms and drag it onto the canvas  
  
![image](https://user-images.githubusercontent.com/101945531/223024876-4a2fb69b-74d5-400e-a4df-6581edef0ccd.png)

  
<li> Data transformation section drag Split data module onto the canvas and connect the dataset’s output port to the Split data module. Simply drag from the dataset’s output port to the Split data module’s input port.
  
![image](https://user-images.githubusercontent.com/101945531/223025034-499939e6-0851-47b6-85e1-9184b98d9964.png)
  
 <li> Machine Learning Algorithms and under Regression select the Linear Regression module and drag it onto the canvas
   
 ![image](https://user-images.githubusercontent.com/101945531/223025145-2c45a968-1bbb-4bdc-b173-0c9ac7fafa98.png)

   
<li> Model Training section, select Train Model. Connect the output port of the Linear Regression module to the left input port of the Train Model module. Connect the left port (training set) of the Split Data module to the right input port.
  
 ![image](https://user-images.githubusercontent.com/101945531/223025275-822f80b0-6850-4953-8a77-76fcba8e2ea9.png)

  <li> Select the Train Model module and in the right pane click on Edit column to select the label column (the variable that you want to predict).
    
 ![image](https://user-images.githubusercontent.com/101945531/222965924-2e9f5970-2dd0-44d7-bf63-54955c20520b.png)

<li> Model Scoring and Evaluation section, select the Evaluate Model module. Connect the output of the Score Model module to the left input of the Evaluate Model module
  
![image](https://user-images.githubusercontent.com/101945531/223025504-615579dc-091c-4b87-baf7-0ab8680a825d.png)
  
<br>
  
![image](https://user-images.githubusercontent.com/101945531/223025569-bde733ca-be4f-4d53-b89c-840881f099e2.png)

  ## Training model
  
![image](https://user-images.githubusercontent.com/101945531/223025887-181d496f-156b-412c-a138-f48db96e4977.png)


  
  ## Set up Compute target
  
 <li> Select the settings icon. In the setting pane, under Default compute target click on Select compute target.
 
 ![image](https://user-images.githubusercontent.com/101945531/222966104-ba1d8d11-55aa-4205-b7cc-3b681b76f03e.png)
  
 <li> Depends on your need create compute target ( cpu/gpu core is high time consumption will be reduced)
   
 ![image](https://user-images.githubusercontent.com/101945531/222966152-7911ac81-0dbd-4729-a6d5-e5addaad6a1a.png)
      
<br>
      
 [image](https://user-images.githubusercontent.com/101945531/222966182-4a0f8e54-06b4-4cbc-9ac4-3414193b7e93.png)
   
 ## Run the training pipeline
   
<li> Set up pipeline run form, select Create new, enter a name for the experiment and click Submit. 
  
![image](https://user-images.githubusercontent.com/101945531/222966252-317fd4c9-c68e-462c-8752-7ea6e0538f14.png)
  
 <li> Monitor the pipeline job run
   
 ![image](https://user-images.githubusercontent.com/101945531/222966287-d4e90865-e788-4bba-870c-419aa7e5a2fb.png)
   
 ## Result 
   
 <li>Right-click the Score Model and select Visualize > Scored dataset. The last two columns of the dataset are the actual and the predicted CO2 emissions
   
 ![image](https://user-images.githubusercontent.com/101945531/222966324-a3b0ec8f-e7e9-4b5c-91a3-379c4c0deb32.png)

  
   

     

