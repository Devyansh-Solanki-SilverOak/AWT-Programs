## Code for calling our functions ##
```
try{
    if(simplyInsurance && typeof simplyInsurance !== "undefined" )
        simplyInsurance.loadApp();
}catch(e){
    console.log(e);
}
```

## Title ##
```
<div class="si-widget"></div>
<img width="1" height="1" alt="shipping protection" style="width: 1px;height: 1px;" onLoad="simplyInsurance.loadApp();" src="data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==" />
```
