1. The “this” keyword refers to the object that the function is a property of.
```
function doSomething() {
  console.log(this);
}
   
doSomething();
```
2. Since the function is invoked in the global context, the function is a property of the global object.
3. Therefore, the output of the above code will be the global object. Since we ran the above code inside the browser, the global object is the window object.
4. Example 2:
```
var obj = {
    name:  "vivek",
    getName: function(){
    console.log(this.name);
  }
}
   
obj.getName();
```
5. In the above code, at the time of invocation, the getName function is a property of the object obj , therefore, this keyword will refer to the object obj, and hence the output will be “vivek”.
6. Example 3:
```
 var obj = {
    name:  "vivek",
    getName: function(){
    console.log(this.name);
  }
     
}
       
var getName = obj.getName;
       
var obj2 = {name:"akshay", getName };
obj2.getName();
```
7. Although the getName function is declared inside the object obj, at the time of invocation, getName() is a property of obj2, therefore the “this” keyword will refer to obj2.
8. The silly way to understand the “this” keyword is, whenever the function is invoked, check the object before the dot. The value of this . keyword will always be the object before the dot.
9. If there is no object before the dot-like in example1, the value of this keyword will be the global object.
10. Example 4:
```
var obj1 = {
    address : "Mumbai,India",
    getAddress: function(){
    console.log(this.address); 
  }
}
   
var getAddress = obj1.getAddress;
var obj2 = {name:"akshay"};
obj2.getAddress();    
```
11. Although in the code above, this keyword refers to the object obj2, obj2 does not have the property “address”‘, hence the getAddress function throws an error.
