# k8s-grafana-prom
λ kubectl apply -f .\nginx-deployment.yaml

λ kubectl apply -f .\nginx-service.yaml

λ kubectl run -it busybox --image=busybox sh
  ..wget http://nginx-service/index.html

λ helm init

λ helm fetch stable/prometheus

λ helm install prometheus stable/prometheus

λ helm install nginx-ingress stable/nginx-ingress

λ kubectl apply -f .\prometheus-ingress.yaml     
ingress.extensions/prometheus-ingress configured

λ helm install grafana stable/grafana

λ kubectl get secret --namespace default grafana -o jsonpath="{.data.admin-password}"

λ kubectl apply -f .\prometheus-ingress.yaml
