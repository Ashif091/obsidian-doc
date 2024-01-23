```js
const user = {
  id: 1,
  name: "John",
  address: {
    city: "New York",
    zipCode: "10001"
  }
};

// Traditional way
const city = user.address ? user.address.city : "Unknown";
console.log(city); // Outputs: "New York"

// Using optional chaining
const cityWithOptionalChaining = user.address?.city ?? "Unknown";
console.log(cityWithOptionalChaining); // Outputs: "New York"

// Accessing a property that doesn't exist
const email = user.email?.toLowerCase() ?? "No email available";
console.log(email); // Outputs: "No email available"

```



page id =  293