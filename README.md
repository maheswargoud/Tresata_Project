

**Prerequisite**

__Terraform install__
__Set Up AWS Credentials :__ aws configure

__Install Kubectl__ https://kubernetes.io/docs/tasks/tools/

__Install Helm__ https://helm.sh/docs/intro/install/
__Update Helm:__ helm repo update

__Install/update latest AWS CLI:__ https://aws.amazon.com/cli/




**Terraform Execution Steps**

__Initialize Terraform :__ terraform init
__Validate the Configuration :__ terraform validate
__Plan the Execution :__ terraform plan
__Apply the Terraform Plan :__ terraform apply


__Configure kubectl for EKS Access :__
aws eks --region us-west-2 update-kubeconfig --name "my-eks-cluster"


kubectl get nodes

kubectl get ns

kubectl get deploy -n prometheus

kubectl get svc -n prometheus



**Grafana setup**

__Verify Services__
kubectl get svc -n prometheus

__edit the Prometheus-grafana service:__
kubectl edit svc prometheus-grafana -n prometheus

__change ‘type:__ ClusterIP’ to 'LoadBalancer'

kubectl get svc -n prometheus

Access the service using the LoadBalancer's external IP

__Username:__ admin 
__Password:__ prom-operator


Import Dashboard ID: 1860


