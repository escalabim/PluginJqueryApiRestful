# PluginJqueryApiRestful
Segue o plugin jquery para consumi Apis Restful usando ajax.
Exemplos de chamadas no seu codigo jquery 

1 USE ALGO ASSIM PARA SE VOCÊ FOR CONSUMIR UMA API COM AUTENTICAÇÃO 'Bearer'

    let token = "********";
    Objdata = {
        " ": " "
    };
    let run = { authorization: true, token: token, control: " ", data: Objdata };
    $.ApiPOST(run).done(function (data) {
    
        let response = JSON.stringify(data);
        let final = JSON.parse(response); 
        
     }).fail(function (jqXHR, textStatus, errorThrown) {       
        if (jqXHR.status == 0) {
           
        } else if (jqXHR.status == 404) {
           
        } else if (jqXHR.status == 500) {
           
        } else if (exception === 'parsererror') {
            
        } else if (exception === 'timeout') {
           
        } else if (exception === 'abort') {
            
        } else {
           
        }
    });


2 USE ALGO ASSIM SE VOCÊ FOR CONSUMIR UMA API SEM AUTENTICAÇÃO 'Bearer'
   
    let run = { authorization: false, control: "" };
    $.ApiGET(run).done(function (data) {
       
        let response = JSON.stringify(data);
        let final = JSON.parse(response);         
         

       }).fail(function (jqXHR, textStatus, errorThrown) {       
        if (jqXHR.status == 0) {
           
        } else if (jqXHR.status == 404) {
           
        } else if (jqXHR.status == 500) {
           
        } else if (exception === 'parsererror') {
            
        } else if (exception === 'timeout') {
           
        } else if (exception === 'abort') {
            
        } else {
           
        }
    });



