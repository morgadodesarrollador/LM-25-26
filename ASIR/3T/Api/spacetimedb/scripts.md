
##### desde build
docker build -t morgadoberruezo/spacetimedb .
docker imgaes
docker push morgadoberruezo/spacetimedb:latest



###### desde helm
kubectl delete ns spacetimedb
helm install spacetimedb . -n spacetimedb --create-namespace -f values.yaml
kubectl get pods -n spacetimedb -w
kubectl logs -n spacetimedb spacetimedb-749dccb7b9-k24lm