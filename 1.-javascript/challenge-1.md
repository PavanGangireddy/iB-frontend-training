# Challenge \#1

* [ ] Now it’s time for the first challenge of the course! Convert the following code into ES6.
* [ ] Use all the concepts you have learned till now

```javascript
function addressMaker(address) {
    var newAddress = {
        city: address.city,
        state: address.state
    };
    if (address.country === undefined) {
        newAddress.country = "India"
    } else {
        newAddress.country = address.country
    }
    return newAddress.city + ", " + newAddress.state + ", " + newAddress.country
}

function studentDetailsLogger(studentDetails) {
    var Address = addressMaker(studentDetails.address)
    console.log(studentDetails.name + " stays in " + Address)
}

var studentDetails = {
    name: "Ramesh",
    gender: "Male",
    address: {
        city: "Kurnool",
        state: "Andhra Pradesh"
    }
}

studentDetailsLogger(studentDetails)

```

