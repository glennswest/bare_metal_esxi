# bare_metal_esxi
Using CRC (Code Ready Containers, to host a metal3 operator that manages esxi hosted machines


## Setup prereqs:
setup.sh

## Add your user to sudoer file


## After installed:
```javascript
oc login -u kubeadmin -p BMLkR-NjA28-v7exC-8bwAk  https://api.crc.testing:6443
oc project metal3
oc get all
NAME                                                      READY   STATUS    RESTARTS   AGE
pod/cluster-api-controller-manager-0                      1/1     Running   0          25m
pod/cluster-api-provider-baremetal-controller-manager-0   2/2     Running   0          25m
pod/metal3-baremetal-operator-599c685865-m8c6t            3/3     Running   0          34m

NAME                                                                    TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
service/cluster-api-controller-manager-service                          ClusterIP   172.30.234.150   <none>        443/TCP    25m
service/cluster-api-provider-baremetal-controller-manager-metrics-svc   ClusterIP   172.30.161.157   <none>        8443/TCP   25m
service/cluster-api-provider-baremetal-controller-manager-service       ClusterIP   172.30.123.99    <none>        443/TCP    25m

NAME                                        READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/metal3-baremetal-operator   1/1     1            1           34m

NAME                                                   DESIRED   CURRENT   READY   AGE
replicaset.apps/metal3-baremetal-operator-599c685865   1         1         1       34m

NAME                                                                 READY   AGE
statefulset.apps/cluster-api-controller-manager                      1/1     25m
statefulset.apps/cluster-api-provider-baremetal-controller-manager   1/1     25m
Glenns-MacBook-Pro-2:manager gwest$ 


