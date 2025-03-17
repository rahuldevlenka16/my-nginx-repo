# my-nginx-repo

# my-nginx-repo
image build:

    docker build -t my-nginx .

    docker tag my-nginx rahuldevsecops/my-nginx:latest


docker hub command:
    docker login -u rahuldevsecops

    generate app pass and use it 

    docker push rahuldevsecops/my-nginx:latest

to run:
    docker run -rm -p 8080:80 rahuldevsecops/my-nginx:latest


--------------------------------------------------------------

kubectl apply -f deploy-my-nginx.yaml

kubectl get pods

kubectl expose deployment my-nginx --type=NodePort --port=80

kubectl get svc

go to:
    localhost:<NodePort>




cleaning:
kubectl delete deployments <deplyoment-name>
kubectl delete deployments --all
kubectl delete service <service-name>
kubectl delete service --all
