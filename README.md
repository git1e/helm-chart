# helm-chart
## create a chart
```
helm create demo-chart
```

## 打包chart
```
helm package demo-chart
```

## 添加描述文件 index.yaml
```
helm repo index --url https://try-001.github.io/helm-chart/ .
```
## 升级chart
```
cp -a demo-chart demo-chart-0.1.1
cd demo-chart-0.1.1/
# 修改版本号
vim Chart.yaml 
# 打包chart
helm package demo-chart-0.1.1/
# 添加描述文件 index.yaml
helm repo index --url https://try-001.github.io/helm-chart/ .
```
## 提交并推送git仓

## 添加repo
```
helm repo add myrepo https://try-001.github.io/helm-chart
```
## 查找
```
helm search repo demo-chart
```
