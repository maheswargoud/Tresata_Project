

**Prerequisite**
Terraform install :
Set Up AWS Credentials : aws configure
Install Kubectl : https://kubernetes.io/docs/tasks/tools/
Install Helm : https://helm.sh/docs/intro/install/
Update Helm : helm repo update
Install/update latest AWS CLI : https://aws.amazon.com/cli/




**Terraform Execution Steps**

Initialize Terraform : terraform init
Validate the Configuration : terraform validate
Plan the Execution : terraform plan
Apply the Terraform Plan : terraform apply


**Configure kubectl for EKS Access**
aws eks --region us-west-2 update-kubeconfig --name "my-eks-cluster"


kubectl get nodes

kubectl get ns

kubectl get deploy -n prometheus

kubectl get svc -n prometheus



**Grafana setup**

Verify Services :
kubectl get svc -n prometheus

edit the Prometheus-grafana service :
kubectl edit svc prometheus-grafana -n prometheus

change ‘type : ClusterIP’ to 'LoadBalancer'

kubectl get svc -n prometheus

Access the service using the LoadBalancer's external IP

Username: admin 
Password: prom-operator


Import Dashboard ID: 1860


