# EBS Dynamic Provisioning  Steps:
==================================================
1. We need to install the EBS CSI drivers in EKS cluster.
kubectl apply -k "github.com/kubernetes-sigs/aws-ebs-csi-driver/deploy/kubernetes/overlays/stable/?ref=release-1.32"
2. Your nodes should have access to connect with EBS volumes. Attach EBS CSI policy to the EC2 instance role.
3. someone on behalf of you should create EBC Volume in AWS and equivalent PV in K8s automatically --> dynamic provisioning that one is Storage class.

$kubectl get sc
$kubectl api-resources

# Run the application in kubernetes

Roboshop templatize helm charts
```
kubectl apply -f namespace.yaml
```
```
kubectl apply -f sc.yaml
```
```
kubectl apply -f mysql/manifest.yaml
```
```
kubectl apply -f mongodb/manifest.yaml
```
```
kubectl apply -f rabbitmq/manifest.yaml
```
```
kubectl apply -f redis/manifest.yaml
```
```
kubectl apply -f catalogue/manifest.yaml
```
```
kubectl apply -f cart/manifest.yaml
```
```
kubectl apply -f user/manifest.yaml
```
```
kubectl apply -f shipping/manifest.yaml
```
```
kubectl apply -f payment/manifest.yaml
```
```
kubectl apply -f web/manifest.yaml
```
```
kubectl apply -f debug/manifest.yaml
```
```
kubectl apply -f dispatch/manifest.yaml
```



