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
  
  * https://www.codewars.com/kata/get-list-sum-recursively/train/javascript/5d158f3306317c0022af2122
  
  ```javaScript```
  
  Get list sum recursively
  
  function sumR(x) {
    if(x.length === 0){
    return 0;
    }else{
    return x.shift () + sumR(x);
    }
  }
  
  * https://www.codewars.com/kata/do-i-get-a-bonus/train/javascript
  
  ```javaScript```
  
  Do I get a bonus?
  
  function bonusTime(salary, bonus) {
    return bonus ? `£${10 * salary}` : `£${salary}`;
  }
  
  * https://www.codewars.com/kata/initialize-my-name/train/javascript/5d182fca0fb98b001c583d46
  
  ```javaScript```
  
  Initialize my name
  
  function initializeNames(name){
    let arr = name.split(' ');
     for (let i = 1; i < arr.length - 1; i++) 
         arr[i] = arr[i].charAt(0) + '.';
     return arr.join(' ');
  }
  merge branch 
  
  * https://www.codewars.com/kata/returning-strings/train/javascript
  
  ```javaScript```
  
  Returning Strings
  
  function greet(name){
    return `Hello, ${name} how are you doing today?`;
  }
  
  * https://www.codewars.com/kata/string-ends-with/train/javascript/5d22c23d3c70c00021be4fd1
  
  ```javaScript```
  
  String ends with?
  
  function solution(str, ending){
   return str.endsWith(ending);
  }
  
  * https://www.codewars.com/kata/spongebob-meme/train/javascript
  
  ```javaScript```
  
  sPoNgEbOb MeMe
  
  function spongeMeme(s) {
    let str = '';
    for(let i = 0; i < s.length; i++){
      if(i % 2 == 0){ str += s[i].toUpperCase();
      }else{ str += s[i].toLowerCase();
      }
  }
  return str;
  }
  
  * https://www.codewars.com/kata/print-a-rectangle-using-asterisks/train/javascript
  
  ```javascript```
  
  Print a Rectangle Using Asterisks
  
  function getRectangleString(w, h) {
    if (w === 1&&h === 1) return '*\r\n'
    if (w === 1&&h === 2) return '*\r\n*\r\n'
      let start = '*' . repeat(w) + '\r\n'
      let mid = '*'+' '.repeat(w - 2) +'*'+'\r\n'
      let end = mid.repeat(h - 2)
    return start + end + start;
  }
  * https://www.codewars.com/kata/maximum-triplet-sum-array-series-number-7/train/javascript
  
  ```javaScript```
  
  Maximum Triplet Sum (Array Series #7)
  
  function maxTriSum(numbers){
    let sum = 0;
      let res = numbers.sort((a, b) => b - a);
      let arr = [];
      for(let i = 0; i < res.length; i++){
        if (arr.length >= 3){
          break
          }
          if(!arr.includes(res[i])){
            arr.push(res[i]);
            sum += res[i];
            }
          }
         return sum;
         
  }
  
  *https://www.codewars.com/kata/string-average/train/javascript
  
  ```javaScript```
  
  String average
  
  function averageString(str) {
    let num = 'zero,one,two,three,four,five,six,seven,eight,nine'.split(',');
    let arr = str.split(/\s/);
    let all = arr.map(s =>num.indexOf(s));
    let avg = all.reduce((a,b) => a + b,0)/arr.length;
    let na = 'n/a';
    return all.some(n =>n<0) ? na : num[Math.floor(avg)] || na;
    
  }
  * 
  
  *https://www.codewars.com/users/Favor/completed_solutions
  
  ```javaScript```
  
  Ordering the words!
  
  function orderWord(s){
   return !s||s.length==0?"Invalid String!":s.split('').sort().join('')
  }
  
  * https://www.codewars.com/kata/numerical-palindrome-number-5-1/train/javascript
  
  ```javaScript```
  
  Numerical Palindrome #5
  
  function palindrome(num) { 
    if(typeof num !== 'number' || num < 0) return "Not valid";
    if(num < 10) return false;
    num = num.toString().split('').sort();
    console.log(num);
    let count = 0;
    for(let i = 0; i < num.length - 1; i){
     if(num[i] === num[i + 1]){
      count = count + 2;
      i = i + 2;
     }else i++;
    }
    if(num.length === count || num.length === count +1){
    return true;
    }else return false;
    
  }
  
  *https://www.codewars.com/kata/are-we-alternate/train/javascript
  
  ```javaScript```
  
  Are we alternate?
  
  function isAlt(word) {
    let vowels = ['a','e','i','o','u'];
    let letters = word.split('');
    for(let i = 0; i < letters.length - 1; i++) {
      if(vowels.includes(letters[i])) {
          if(vowels.includes(letters[i+1])) {
             return false;
         }
      }
      else {
        if(!vowels.includes(letters[i+1])) {
          return false;
          }
       }
     }
      return true;
  }
  
  * https://www.codewars.com/kata/shortest-word/train/javascript
  
  ```javaScript```
  
  Shortest Word
  
  function findShort(s){
      return Math.min(...s.split(" ").map (s => s.length));
  }
  
  * https://www.codewars.com/kata/double-char/train/javascript
  
  ```javaScript```
  
  Double Char
  
  function doubleChar(str) {
    let doubledChar = "";
    for ( let i = 0; i < str.length; i++){
      doubledChar += str[i] + str[i];
  }
  
   return doubledChar;
   }
   
   *https://www.codewars.com/kata/convert-boolean-values-to-strings-yes-or-no/train/javascript
   
   ```javaScript```
   
   Convert boolean values to strings 'Yes' or 'No'.
   
   function boolToWord( bool ){
     if (bool === true) {
      return 'Yes'
      }else{
        return 'No'
      }   
   }
   
   *https://www.codewars.com/kata/simple-simple-simple-string-expansion/train/javascript/5d30bca39946160017b4b994
   
   ```javaScript```
   
   Simple Simple Simple String Expansion
   
   function stringExpansion(s) {
     let res = "", x = 1;
     for (let i = 0; i <s.length; i++)
        (s[i] == +s[i]) ? x = +s[i] : res += s[i].repeat(x);
     return res;
   }
   
   *https://www.codewars.com/kata/mumbling/train/javascript
   
   Mumbling
   
   function accum(s) {
   	let letters = s.toLowerCase().split('')
     for(let i = 0; i < letters.length; i++) {
       letters[i] = letters[i].toUpperCase() + letters[i].repeat(i)
       }
       return letters.join('-')
   }
   
 *https://www.codewars.com/kata/reversed-strings/train/javascript
 
 ```javaScript```
 
 Reversed Strings
 
 function solution(str){
   return str.split('').reverse().join('');
 }
 
 *https://www.codewars.com/kata/string-repeat/train/javascript
 
 ```javaScript```
 
 String repeat
 
 function repeatStr (n, s) {
   return s.repeat(n);
 }
 
 *https://www.codewars.com/kata/bit-counting/train/javascript
 
 ```javaScript```
 
 Bit Counting
 
 var countBits = function(n) {
   return n.toString(2).replace(/0/g,'').length;
 };
 
 *https://www.codewars.com/kata/convert-number-to-reversed-array-of-digits/train/javascript/5d365c557dbc0500206ba545
 
 ```javaScript```
 
 Convert number to reversed array of digits
 
 *https://www.codewars.com/kata/fake-binary/train/javascript
 
 Fake Binary
 
 function fakeBin(x){
   return x.split('').map(function(v){
      return v < 5 ? '0': '1'
   }).join('')
   
   }
   
   *https://www.codewars.com/kata/capitalization-and-mutability/train/javascript
   
   Capitalization and Mutability
   
   function capitalizeWord(word) {
     return word[0].toUpperCase () + word.slice(1);
   }
   
   *https://www.codewars.com/kata/vowel-count/train/javascript
   
   ```javaScript```
   
   Vowel Count
   
   function getCount(str) {
      str = str.toLowerCase();
     var vowels = 'aeiou';
     var vowelCount = 0;
     for(var i = 0; i < str.length; i++) {
       if (vowels.indexOf(str[i]) !== -1) {
         vowelCount++;
       }
     }
     return vowelCount;
   }
     
 
 function digitize(n) {
   return n.toString().split('').reverse().map(Number);
 }
 
 *https://www.codewars.com/kata/you-only-need-one-beginner/train/javascript
 
 ```javaScript```
 
 You only need one - Beginner
 
 function check(a,x){
    if  (a.includes(x)){
     return true;
     } else {
       return false;
     }
 };
 
 *https://www.codewars.com/kata/man-in-the-west/train/javascript
 
 ```javaScript```
 
 Man in the west
 
 function checkTheBucket(bucket){
   return bucket.includes('gold');
 }
 
 *https://www.codewars.com/kata/kata-example-twist/train/javascript
 
 Kata Example Twist
 
 var websites = [];
  while(websites.length < 1000) websites.push("codewars")
  
  *https://www.codewars.com/kata/invert-values/train/javascript
  
  ```javaScript```
  
  Invert values
  
  function invert(array) {
     return array.map(x => x === 0 ? x : - x) ;
  }
  
  *https://www.codewars.com/kata/remove-duplicates-from-list/train/javascript
  
  ```javaScript```
  
  Remove duplicates from list
  
  function distinct(a) {
    return [...new Set(a)];
  }
  
  *https://www.codewars.com/kata/write-shortest-function-to-calculate-average-number-of-array/train/javascript
  
  ```javaScript```
  
  Write shortest function to calculate Average number of Array
  
  function avg(a){
    return a.reduce((a, b)=>a + b,0)/a.length;
  }
  
  *https://www.codewars.com/kata/array-array-array/train/javascript
  
  ```javaScript```
  
  Array Array Array
  
  
  function explode(x){
     if(typeof x[1] === 'number' && typeof x[0] ==='number'){
     const L = x[0] + x[1];
     return Array.from({length : L}).fill(x);
     }
      if(typeof x[1] ==='number' || typeof x[0] ==='number'){
      let L = 0;
      typeof x[0] ==='number'?L=x[0]:L=x[1]
      return Array.from({length : L}).fill(x)
      }
       if(typeof x[1] !=='number'&& typeof x[0] !=='number'){
      return 'Void!'
      }
  }
  
  *https://www.codewars.com/kata/a-gift-well-spent/train/javascript
  
  ```javaScript```
  
  A Gift Well Spent
  
  var buy = function(x, arr){
    for(var i= 0; i < arr.length -1; ++i)
      for(var j =i +1; j < arr.length; ++j)
        if(arr[i] + arr[j] == x)
          return [i, j]
    return null;
  };
  
  *https://www.codewars.com/kata/building-blocks/train/java/5d42587938e42e0026598f81
  
  ```java```
  
  Building blocks
  
  public class Block {
      private int width;
      private int length;
      private int height;
  
      public int getWidth() {
          return width;
      }
  
      public int getLength() {
          return length;
      }
  
      public int getHeight() {
          return height;
      }
  
      public Block(int[] arr) {
          this.width = arr[0];
          this.length = arr[1];
          this.height = arr[2];
      }
  
      public int getVolume(){
          return width * length * height;
      }
  
      public int getSurfaceArea(){
          return 2 * (width * length + width * height + length * height);
      }
  }
  
  *https://www.codewars.com/kata/lombok-encapsulation/train/java/5d4255d038f6750024638ccc
  
  ```java```
  
  Lombok Encapsulatio
  
  public class EncapsulationDemo {
      private int number;
      private String stringValue;
      private Object anObject;
  
      public int getNumber() {
          return number;
      }
  
      public void setNumber(int number) {
          this.number = number;
      }

      
  
      public String getStringValue() {
          return stringValue;
      }
  
      public void setStringValue(String stringValue) {
          this.stringValue = stringValue;
      }
  
      public Object getAnObject() {
          return anObject;
      }
  
      public void setAnObject(Object anObject) {
          this.anObject = anObject;
      }
  
      public EncapsulationDemo() {
      }
  
      public EncapsulationDemo(int number, String stringValue, Object anObject) {
          this.number = number;
          this.stringValue = stringValue;
          this.anObject = anObject;
      }
  }
  
  *https://www.codewars.com/kata/playing-with-cubes-i/train/java/5d42377bd885f90019935650
  
  ```java```
  
  Playing with cubes I
  
  public class Cube {
      int side;
  
      int getSide(){
        return side;
      }
  
      void setSide(int side){
          this.side = side;
      }
  
  }
  
  *https://www.codewars.com/kata/a-needle-in-the-haystack/train/javascript
  
  ```javaScript```
  
  A Needle in the Haystack
  
  function findNeedle(haystack) {
    return "found the needle at position " + haystack.indexOf("needle");
  }
  
  *https://www.codewars.com/kata/will-you-make-it/train/javascript
  
  ```javaScript```
  
  Will you make it?
  
  const zeroFuel = (distanceToPump, mpg, fuelLeft) => {
    return mpg * fuelLeft >= distanceToPump;
  };
  
  *https://www.codewars.com/kata/century-from-year/train/javascript
  
  ```javaScript```
  
  Century From Year
  
  function century(year) {
    return Math.ceil(year/100);
  }
  
  *https://www.codewars.com/kata/third-angle-of-a-triangle/train/javascript
  
  ```javaScript```
  
  Third Angle of a Triangle
  
  function otherAngle(a, b) {
    return 180-(a + b);
  }
  
  *https://www.codewars.com/kata/discover-the-original-price/train/javascript
  
  ```javaScript```
  
  Discover The Original Price
  
  function discoverOriginalPrice(discountedPrice, salePercentage){
    return(discountedPrice/((100-salePercentage))*100).toFixed(2)*1
  }




 
   
   
   

