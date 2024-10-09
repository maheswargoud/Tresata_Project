

**Prerequisite**

__Terraform install :__ https://developer.hashicorp.com/terraform/install
__Set Up AWS Credentials :__ aws configure
__Install Kubectl :__ https://kubernetes.io/docs/tasks/tools/
__Install Helm :__ https://helm.sh/docs/intro/install/
__Update Helm :__ helm repo update
__Install/update latest AWS CLI :__ https://aws.amazon.com/cli/





**Terraform Execution Steps**

__Initialize Terraform :__ terraform init
__Validate the Configuration :__ terraform validate
__Plan the Execution :__ terraform plan
__Apply the Terraform Plan :__ terraform apply





**Configure kubectl for EKS Access**
aws eks --region us-west-2 update-kubeconfig --name "my-eks-cluster"

kubectl get nodes
kubectl get ns
kubectl get deploy -n prometheus
kubectl get svc -n prometheus






**Grafana setup**

__Verify Services :__
kubectl get svc -n prometheus

__edit the Prometheus-grafana service :__
kubectl edit svc prometheus-grafana -n prometheus

__change ‘type :__ ClusterIP’ to 'LoadBalancer'

kubectl get svc -n prometheus

Access the service using the LoadBalancer's external IP

__Username:__ admin 
__Password:__ prom-operator


__Import Dashboard ID:__ 1860


