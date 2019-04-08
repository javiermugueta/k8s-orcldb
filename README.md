# oracle database on k8s

## get credentials to container-registry.oracle.com
You must accept the licence agreement!!!

## deployment steps:
```
kubectl create secret docker-registry oradocreg --docker-username=<youruser> --docker-password=<yourpassword> --docker-server=container-registry.oracle.com

kubectl apply -f https://raw.githubusercontent.com/javiermugueta/k8s-orcldb/master/orcldb.yaml
```
## further config steps

````
kubectl get pods

MacBook-Pro:~ javiermugueta$ kubectl get pods
NAME                      READY   STATUS    RESTARTS   AGE
orcldb-xxxxxxxxx   1/1     Running   0          15m

kubectl exec -it orcldb-xxxxxxxxx -- bash

[oracle@orcldb-xxxxxxxxx /]$ sqlplus / as sysdba
SQL*Plus: Release 12.2.0.1.0 Production on Mon Apr 8 22:16:22 2019
Copyright (c) 1982, 2016, Oracle.  All rights reserved.
Connected to:
Oracle Database 12c Enterprise Edition Release 12.2.0.1.0 - 64bit Production
SQL> alter user sys identified by whatyouwant;
User altered.
SQL>create user ainos identified by tusabras default tablespace users temporary tablespace temp;
SQL>alter user ainos quota unlimited on users;
SQL>grant connect, resource to ainos;
SQL>grant create materialized view to ainos;
SQL>exit
[oracle@orcldb-xxxxxxxxx /]$exit
```