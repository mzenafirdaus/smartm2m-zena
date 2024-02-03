![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/1cc39772-f4e7-4e7d-aebb-0a679226c13a)


Rolling Update to Nginx Version 1.11.13-alpine

microk8s kubectl set image deployment/nginx-app nginx=nginx:1.11.13-alpine -n smartm2m
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/506d8671-1d91-4acd-8a8d-6e2a17dcff6d)
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/1618b660-ec44-48e8-a17a-bd7cd0ae493b)

Rollback Update to Nginx Version 1.11.10-alpine

kubectl rollout undo deployment/nginx-app -n smartm2m
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/2cac8f14-0fe3-4d5e-95d2-816268868ee1)

Set Node k8s-node-1 as Unavailable and Reschedule Pods

microk8s kubectl cordon master

![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/ebea93f1-3c9c-4ab7-a04c-bb2164429fdb)

microk8s kubectl drain master --delete-emptydir-data --ignore-daemonsets
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/dac80e4c-bf1e-45f6-8212-4935933ffdef)

microk8s kubectl apply -f app-data.yaml -n smartm2m
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/7def822f-c902-482e-a021-899eeefb36c1)

microk8s kubectl apply -f pvc.yaml -n smartm2m
![image](https://github.com/mzenafirdaus/smartm2m-zena/assets/85167578/e2305a01-308a-4de3-9afe-7a4ba61af68a)
