## callback hell
The phenomenon which happens when we nest multiple callbacks within a function is called a callback hell. The shape of the resulting code structure resembles a pyramid and hence callback hell is also called the “pyramid of the doom”. It makes the code very difficult to understand and maintain.
  
```
  getArticles(20, (user) => {
  console.log("Fetch articles", user);
  getUserData(user.username, (name) => {
    console.log(name);
    getAddress(name, (item) => {
      console.log(item);
      // this goes on and on...
    }
})
```
- Ways to escape callback hell
  1. Promise
  ```
  getArticles(10)
  .then((user) => getUserName(user.name))
  .then((place) => getAddress(place.city))
  .then((data) => console.log("Data", data))
  .catch((err) => console.log("Error: ", err.message));
  ```
