# Chapter 10 – Promises ⭐⭐⭐⭐⭐
- Promise JavaScript ka ek object hai jo batata hai ki koi asynchronous (time lene wala) task future me complete hoga ya fail hoga. React me API call, database request aur file upload sab Promises par based hote hain.

## Promise Kya Hai?
Real-life example:

Socho tumne Swiggy ya Zomato se food order kiya.

- Order Place ✔️
- Food Prepare ⏳
- Delivered ✅
- Ya Cancel ❌

Jab tak result nahi aata, order Pending state me hota hai.

Promise bhi bilkul aisa hi kaam karta hai.

## Promise States

<code><pre>
Pending
        │
        ├── Fulfilled (Success)
        │
        └── Rejected (Failed)
</pre></code>

**1. Pending**

Task abhi chal raha hai.

**2. Fulfilled**

Task successfully complete ho gaya.

**3. Rejected**

Task fail ho gaya.

**Promise Syntax**

const promise = new Promise((resolve, reject) => {

});
- resolve() → Success
- reject() → Failure

## Success Example
<code><pre>
const promise = new Promise((resolve, reject) => {
    resolve("Data Loaded Successfully");
});

promise.then(data => {
    console.log(data);
});
</pre></code>

**Output**
- Data Loaded Successfully

## Failed Example
<code><pre>
const promise = new Promise((resolve, reject) => {
    reject("Something went wrong");
});

promise.catch(error => {
    console.log(error);
});
</pre></code>

**Output**
- Something went wrong
