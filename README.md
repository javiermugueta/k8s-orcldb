# k8s-orcldb
An Oracle dababase container image that can be deployed in k8s maintaining persistence

# For deploying in k8s execute the following:
```
kubectl apply -f https://raw.githubusercontent.com/javiermugueta/k8s-orcldb/master/orcldb.yaml
```
---
# How we did it
After pulling the original image in a local machine, it has been pushed here https://hub.docker.com/r/javiermugueta/oracledb/ just for testing/trainig purposes


# Original image
It is located in the Oracle Container Registry repo here:

https://container-registry.oracle.com/pls/apex/f?p=113:4:::NO:4:P4_REPOSITORY,AI_REPOSITORY,AI_REPOSITORY_NAME,P4_REPOSITORY_NAME,P4_EULA_ID,P4_BUSINESS_AREA_ID:9,9,Oracle%20Database%20Enterprise%20Edition,Oracle%20Database%20Enterprise%20Edition,1,0&cs=3XaeaNArKTcAXlOc8rm0jwXqEeF0DDPNO7OAJSihKImvpeAPivAS9ZcwjXEzRR9k5AepESF4EKZSfNTu_g7k2aA
NOTE: Read an abide the licensing constraints
