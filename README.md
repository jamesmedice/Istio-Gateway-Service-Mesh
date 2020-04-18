
 kubectl edit svc istio-ingressgateway -n istio-system

 skaffold run

 kubectl get svc istio-ingressgateway -n istio-system

 kubectl -n istio-system get service istio-ingressgateway -o jsonpath='{.status.loadBalancer.ingress[0].ip}'
 kubectl port-forward -n istio-system $(kubectl get pod -n istio-system -l app=jaeger -o jsonpath='{.items[0].metadata.name}') 16686:16686
 kubectl port-forward -n istio-system $(kubectl get pod -n istio-system -l app=jaeger -o jsonpath='{.items[0].metadata.name}') 16686:16686


 kubectl get gateway 
 kubectl get virtualservice


 kubectl delete gateway product-gateway
 kubectl delete virtualservice product-virtual-service
 kubectl delete -n default service product-service
 kubectl delete -n default deployment product-service-v1