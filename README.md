# EKS-WordPress-MYSQL
this project involves deploying WordPress and MySQL on Amazon EKS.

Change the Nodeaffinity labels as your node
  Here I am using my node name as a value you can give your node Hostname there only mysql pod will deploy.
    -     nodeSelectorTerms:
         - matchExpressions:
           - key: kubernetes.io/hostname
             operator: In
             values:
             <- ip-10-0-127-96.ec2.internal>  # this is my Node hostname
