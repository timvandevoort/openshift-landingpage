s2i build . centos/php-71-centos7 demoapp
```
---> Installing application source...
=> sourcing 20-copy-config.sh ...
---> 13:59:36     Processing additional arbitrary httpd configuration provided by s2i ...
=> sourcing 00-documentroot.conf ...
=> sourcing 50-mpm-tuning.conf ...
=> sourcing 40-ssl-certs.sh ...
Build completed successfully
```

docker run -e CUSTOMER=somecustomer -p 8080:8080 demoapp
```
=> sourcing 20-copy-config.sh ...
---> 13:59:42     Processing additional arbitrary httpd configuration provided by s2i ...
=> sourcing 00-documentroot.conf ...
=> sourcing 50-mpm-tuning.conf ...
=> sourcing 40-ssl-certs.sh ...
AH00558: httpd: Could not reliably determine the server's fully qualified domain name, using 172.17.0.2. Set the 'ServerName' directive globally to suppress this message
[Tue Oct 23 13:59:42.562159 2018] [ssl:warn] [pid 1] AH01909: 172.17.0.2:8443:0 server certificate does NOT include an ID which matches the server name
```
