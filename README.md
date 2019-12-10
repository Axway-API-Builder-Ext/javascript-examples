# API-Builder Javascript Flow-Node examples
The Axway API-Builder Javascript-Flow node provides you flexibility as API-Builder is using Javascript-Objects under the hood. 
The examples listed on this page should help you to make easily use of it for some use-cases.


## Overview
- [Rename Key in a Java-Script Object](#rename-key-in-a-java-script-object)
- [Trace message to console](#create-a-trace-message)

---

## Examples

### Rename Key in a Java-Script Object
If you would like to rename an existing Javascript-Object key, for instance before converting it back to a JSON-String you can use the following code:
```javascript
async function code(data) {
  Object.defineProperty(data, "newKey", 
     Object.getOwnPropertyDescriptor(data, "oldKey")
  );
  delete data["oldKey"];
  return data;
}
```

### Create a Trace message
In the Javascript Flow-Node turn on the `Unsafe Mode` and with that you can log message to the console:
```javascript
async function code(data) {
  console.log("Your message to log")
}
```
