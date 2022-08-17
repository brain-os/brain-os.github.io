## Multivariate Model - In Process Invocation

Steps
1. **Model repository** -Onboard model 
   1. model file 
   2. model specification (input and output), 
   3. dependencies, 
   4. model type (Tensor flow/Scikit Learn/PyTorch/Keras), 
   5. python version, 
   6. input/out data format - numpy or tensor
2. **ML Process Configuration** (on ui) - Part of Brain OS 
   1. URl/Port (Model repository)
   2. model id/version, 
   3. field mapping - Brain Event to model input and output
3. Deployment - will take 
4. Initialization (When model is loaded from model repository)
5. Execution Phase 
   1. Message received from input topic
   2. Input parameter translation
   3. Predict is called
   4. Output parameter translated
   5. Message sent to output topic

```java
interface Model {
    void init();
    double[] predict(double [] input);
    cleanup();
}
```
## Image Classification - In Process Invocation
TODO
Phases
1. Configuration
2. Deployment
3. Initialization (When model is loaded from model repository)
4. Execution Phase
   1. Message received from input topic
   2. Input parameter translation
   3. Predict is called
   4. Output parameter translated
   5. Message sent to output topic

## Remote model invocation
Bridge will play important part
1. **ML Process Configuration** (on ui) - Part of Brain OS
   1. URl/Port (Model invocation end point)
   3. field mapping - Brain Event to model input and output
2. Deployment is only for bridge
4. Execution Phase
   1. Message received from input topic
   2. Input parameter translation
   3. Call remote model thru rest end point
   4. Output parameter translated
   5. Message sent to output topic

