# Angular-Material-Data-Table

~~~
Cloud URL: https://corona-app.cfapps.io/
~~~~


## Command Used
~~~
ng new CoronaClient
ng g c components/CoronaClientComponent --skipTests -is --selector=app-corona --flat true
ng g s services/CoronaClientService --skipTests 
ng add @angular/material
ng build --prod
~~~


  
## Cloud Deployment

Copy this manifest.yml to dist folder for deploy in PCF
~~~	
---
applications:
- name: corona-app
  instances: 1
  memory: 512M
  disk-quote: 1024M
  buildpack: staticfile_buildpack
  domain: cfapps.io
~~~
## Use below comand to push to PCF
~~~
cf login -a http://api.run.pivotal.io -u %USERNAME% -p %PASSWORD%
cf push
~~~

## Consumed API
~~~
Swagger Docs: https://corona.lmao.ninja/docs/
URL: https://corona.lmao.ninja/v2/countries
~~~
