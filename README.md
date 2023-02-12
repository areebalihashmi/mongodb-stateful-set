# mongodb-stateful-set
To setup mongodb in kubernetes efficiently


Step 1: First we need to create PVC for storing the data of mongo such that it wont be lost even if the pod is restarted or deleted.
The file in which we are configuring the PVC definition is pvc.yaml
To apply it use command: **kubectl create -f pvc.yaml -n mynamespace**

Step 2: Create a stateful set for creation of stateful set resource
To apply it, use command: **kubectl apply -f statefulsetdefinition.yaml -n mynamespace**

Step 3: Create a headless service so that we can directly access the pod using pod IP:
To apply it, use command: **kubectl apply -f headless.yaml -n mynamespace**

