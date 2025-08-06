ingress and load balancer both are different

to access the application service clusterIP is not support to access because it is used to access internal not with internet

To access the application service Nodeport is support but nodeport is access by everyone its not for good practise.

To access the application Load Balancer service is support but to access different different pods different different 
load balancer are created.
ex: 100 applications --- 100 load balancer should be created and its high cost

to avoid the high cost we use ingress

ingress also give 3rd party ELB

To implement of ingress we follow some steps:

step 1.install ingress controller

step 2. Ingress resource service

step 3. path-1 deployment

step 4. path-2 deployment

ingress is used for to access the mutliple pods at a time instead for creating multiple load balancer for every pod.
