# **dnslookup** _microservice_
## API to translate Kubernetes service names to IPs and serve them to Lambda functions

## **Prerequisites**:
* ### **Language**: Python 2.7.*
* ### **Predefined variables**: KUBEDNS_IP, DNSLOOKUP_API_KEY
### **Get kubedns IP**
SSH into **devkube-bastion** instance and run:
```
$ dig +noall +answer @<KUBEDNS_IP> <service>.default.svc.cluster.local | awk '{print $5}'
```
### **HTTP Request**
```
https://api.cleanchoiceenergy.io/dnslookup/<servicename>
```
```
curl -i -H 'x-api-key: <DNSLOOKUP_API_KEY>' https://api.cleanchoiceenergy.io/dnslookup/<servicename>
```
<!-- Code goes here -->
