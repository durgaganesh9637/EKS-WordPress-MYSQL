# EKS-WordPress-MYSQL
this project involves deploying WordPress and MySQL on Amazon EKS.


Clone this Repo


Check Replace 1 and 2 files 

kubectl apply -f StorageClass.yaml

kubectl apply -f mysql

kubectl get all
#after mysql resources created(wait for 5 mins)

kubectl apply -f wordpress

kubectl get all
