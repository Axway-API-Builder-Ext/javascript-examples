# API-Builder Javascript Flow-Node examples
The Axway API-Builder Javascript-Flow node provides you flexibility as API-Builder is using Javascript-Objects under the hood. 
The examples listed on this page should help you to make easily use of it for some use-cases.


## Overview
- [Rename Key in a Java-Script Object](#rename-key-in-a-java-script-object)

---

## Examples

### Rename Key in a Java-Script Object
If you would like to modify an existing Javascript-Object key, for instance before converting it back to a JSON-String, you want 
to rename a key.

```js
async function code(data) {
  Object.defineProperty(data, "newKey", 
     Object.getOwnPropertyDescriptor(data, "oldKey")
  );
  delete data["oldKey"];
  return data;
}
```
