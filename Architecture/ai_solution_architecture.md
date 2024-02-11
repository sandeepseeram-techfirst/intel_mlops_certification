#### AI Solution Architectures 

- Code Reusability 
- Maintainability 
- Extensibility 


#### Design 1 - Pipeline Solution Architecture 
provides a structured composition of sequential or parallel processing steps for tasks like data preprocessing, model training and inference stages. 

##### Stages: 
Data Processing =============> Model Development ==============> Inference Service 

#### Design 2 - Model Serving Architecture 
- The Model-Serving solution architecture centers on deploying and utilizing trained models in production environments, enabling their accessibility for making predictions or providing insights. 

- The architecture involves designing a system capable of handling incoming requests, preprocessing input data, applying it to the trained model, and returning predictions or results to the requester. 

- Leverages technologies and frameworks like TorchServe, Tensorflow Serving, OpenVINO Model Server, MLflow Models, ONNX. 

