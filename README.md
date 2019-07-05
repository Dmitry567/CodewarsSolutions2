* https://www.codewars.com/kata/create-phone-number/train/javascript

```javaScript```

Create Phone Number

function createPhoneNumber(numbers){
  let formatPhone = [];
  for(let i=0; i<numbers.length; i++){
    if(i === 0){
      formatPhone.push('(' + numbers[i]);
    } else if(i === 2){
      formatPhone.push(numbers[i] + ')');
    } else if(i === 3){
      formatPhone.push(' ' + numbers[i]);
    } else if(i === 5){
      formatPhone.push(numbers[i] + '-');
    } else {
      formatPhone.push(numbers[i]);
    }
}
return formatPhone.join('');
}   

* https://www.codewars.com/kata/credit-card-issuer-checking/train/javascript

 ```javaScript```
 
 Credit card issuer checking
 
 function getIssuer(number) {
   if (/^3[4|7]\d{13}$/.test(number)) return 'AMEX'
   if (/^6011\d{12}$/.test(number)) return 'Discover'
   if (/^5[1-5]\d{14}$/.test(number)) return 'Mastercard'
   if (/^4(\d{12}|\d{15})$/.test(number)) return 'VISA'
   return 'Unknown'
 }
 
 *https://www.codewars.com/kata/remove-string-spaces/train/javascript
 
 ```javaScript```
 
  Remove String Spaces
  
  function noSpace(x){
   return x.replace(/\s/g, ''); 
  }