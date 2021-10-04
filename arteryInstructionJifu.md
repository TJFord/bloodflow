Navigate to artery.fe folder, e.g., > /data3/tan/bloodflow
You can check what docker images are available on our cluster
``` docker images```
It will list out all the images available. Then we use the image id to load the container
``` docker container run c2619 ```
Activate the fenicsproject. 
``` fenicsproject run ```
You will see the prompt at your terminal will be changed to fenics@SOME_ID
Then, you can run artery.fe demon. Just make sure it is in the right folder.
``` python3 demo_arterybranch.py config/demo_arterybranch.cfg ```
then the code will run and generate some output in folder output. 
for post analysis, 
    ```python3 postprocess.py output/4cycles_last/data.cfg ```
However, currently the postprocess.py is not working
