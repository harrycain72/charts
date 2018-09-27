# How to get the idtoken via REST
```
curl -X POST https://cvm22424.bmwgroup.net/auth/realms/kubernetes-mykc-prod/protocol/openid-connect/token \
-d grant_type=password \
-d client_id=central-grafana \
-d client_secret=7139acca-8776-4392-8b4f-93fffdbacca5 \
-d username=q186379 \
-d password=mypassword \
-d scope=openid \
-d response_type=id_token \
| jq -r '.id_token'
```