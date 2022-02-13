# kubernetes-deploy-tutorial
This code is made for my youtube channel and corresponding to video given below.


<p align="center"> 
    <a href="https://youtu.be/XQNNAeyMAkk" target="_blank">
    <img src="http://img.youtube.com/vi/XQNNAeyMAkk/0.jpg"></img>
  </a>
</p>




minikube start

eval $(minikube -p minikube docker-env)



docker build -t flask-kubernetes .
docker run -p 5000:5000 flask-kubernetes
kubectl apply -f deployment.yaml
minikube dashboard
minikube service flask-test-service



......

when installing minikube - ...


kubectl create deployment hello-minikube --image=8s.gcr.io/echoserver-arm:1.8
kubectl expose deployment hello-minikube --type=NodePort --port=8080
kubectl get services hello-minikube

minikube

instructions:

https://minikube.sigs.k8s.io/docs/start/



https://github.com/kubernetes/minikube/issues/12833



the docker image k8s.gcr.io/echoserver:1.4 is not compatible to the Mac M1 arm64 architecture. A suggestion for your tutorial would be the following:




