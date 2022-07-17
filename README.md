# Building-a-Feature-Engineering-Pipeline-with-Tensorflow-Extended-TFX-
This project builds a feature engineering pipeline using the Metro Interstate Traffic Volume Dataset

![image](https://user-images.githubusercontent.com/69100847/179390021-c651171e-ffb5-41c0-923a-88554a1aa8b0.png)



**Imports**

![image](https://user-images.githubusercontent.com/69100847/179389860-ad0943cd-a5a2-45b1-b510-7e49eec57ff3.png)


**Define paths**

![image](https://user-images.githubusercontent.com/69100847/179389876-14dfc3a0-65f7-4e52-9a92-10fce3ae4588.png)


**Preview Dataset**

![image](https://user-images.githubusercontent.com/69100847/179389882-198f083b-f0de-4fdf-95d2-7637b29df72c.png)


**Interactive Context**

- We need to instantiate the Interactive Context so that different components can run interactiely.
- We will define the metadata store in the pipeline root.


**ExampleGen**

- The ExampleGen is the first component in the pipeline.
- ExampleGen ingests data from external resources such as CSV files 
- ExampleGen produces examples that will be used and read by other TFX Components.

The ExampleGen performs three main functions which are
-  Split the data(default is 2/3 training and 1/3 evaluation).
-  Converts each row of the training data into tf.train.example which is a protocol puffer used to serialize structured data.
-  Compress and save the data in the pipeline root making it optimized for other components to access.

**Running ExampleGen**
![image](https://user-images.githubusercontent.com/69100847/179390498-8cc54823-16dc-4e47-bfec-f90270100927.png)


![image](https://user-images.githubusercontent.com/69100847/179390510-c7d044e5-4140-49c0-98d6-13b4b100eac4.png)






