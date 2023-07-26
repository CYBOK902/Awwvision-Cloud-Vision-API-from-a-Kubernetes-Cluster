# -Awwvision-Cloud-Vision-API-from-a-Kubernetes-Cluster

gcloud auth list
gcloud config list project

Task-1
gcloud config set compute/zone us-central1-a
gcloud container clusters create awwvision \
--num-nodes 2 \
--scopes cloud-platform

gcloud container clusters get-credentials awwvision
kubectl cluster-info

Task-2
sudo apt-get install -y virtualenv
python3 -m venv venv
source venv/bin/activate

Task-3
gsutil -m cp -r gs://spls/gsp066/cloud-vision .

Task-4
cd cloud-vision/python/awwvision
make all

Task-5
kubectl get pods
kubectl get deployments -o wide
kubectl get svc awwvision-webapp
