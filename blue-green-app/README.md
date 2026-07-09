kubectl argo rollouts list rollouts
kubectl argo rollouts status simple-rollout
kubectl argo rollouts get rollout simple-rollout

kubectl argo rollouts set image simple-rollout webserver-simple=docker.io/kostiscodefresh/gitops-canary-app:v2.0 （真实是git仓库修改代码）
kubectl argo rollouts promote simple-rollout 完成测试后，我们可以将所有流量切换到新的版本
kubectl argo rollouts get rollout simple-rollout --watch 观察转移过程
