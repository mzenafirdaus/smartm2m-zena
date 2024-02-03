#Rolling Update to Nginx Version 1.11.13-alpine
kubectl set image deployment/nginx-app nginx=nginx:1.11.13-alpine --record

#Rollback Update to Nginx Version 1.11.10-alpine
kubectl rollout undo deployment/nginx-app

#Set Node k8s-node-1 as Unavailable and Reschedule Pods
kubectl drain k8s-node-1 --ignore-daemonsets
