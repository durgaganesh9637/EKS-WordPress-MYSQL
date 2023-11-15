# EKS-WordPress-MYSQL
this project involves deploying WordPress and MySQL on Amazon EKS.


Replace -1
mysql/mysql-PersistentVolume.yaml
In the mysql-PersistentVolume.yaml file, find the section related to Node Affinity labels. 
Look for the 'values' field under 'matchExpressions' and replace <- ip-10-0-127-96.ec2.internal>
with the hostname of your specific node. 
This step is crucial for directing the MySQL pod to deploy exclusively on the designated node. -     nodeSelectorTerms:
         - matchExpressions:
           - key: kubernetes.io/hostname
             operator: In
             values:
             <- ip-10-0-127-96.ec2.internal>  # this is my Node hostname
Replace -2
mysql/mysql-PersistentVolume.yaml
"Fix mounting issues in mysql/mysql-PersistentVolume.yaml by setting the local path to an existing location on your Kubernetes node for the 'wordpress-volume' PersistentVolumeClaim."
 I have given / as a path because it will be there in all nodes

   local:
    path: /

