helm upgrade -i spring-boot-demo -n spring-boot-demo  myrepo/jlgl-spring-chart --set image.tag=latest \
--set replicaCount=2 \
--set resources.limits.cpu=100m  \
--set resources.limits.memory=100mi \
--set resources.requests.cpu=100m  \
--set resources.requests.memory=100mi \
--set livenessProbe.httpGet.path=/  \
--set livenessProbe.httpGet.port=80 \
--set readinessProbe.httpGet.path=/ \
--set readinessProbe.httpGet.port=80 \
--wait \
--atomic \
--timeout  1m