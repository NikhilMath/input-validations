# [Link for Live view of code](https://fanciful-concha-ef10fe.netlify.app/)

### HTML

```html
    <!-- -------------------------------- html --------------------------------- -->
    <div>
      <form name="FormName" method="POST" action="/cgi-bin/script.cgi">
        <input type="text" name="FieldA" size="19" />
        <input type="text" name="FieldB" size="19" />
        <input
          type="submit"
          onclick="return BothFieldsIdenticalCaseSensitive();"
          value="Click Me"
        />
      </form>
    </div>
```

### JavaScript

```js
function BothFieldsIdenticalCaseSensitive() {
  var one = document.FormName.FieldA.value;
  var another = document.FormName.FieldB.value;
  if (one == another) {
    return true;
  }
  alert("Oops, both fields must be identical.");
  return false;
}

function BothFieldsIdenticalCaseInsensitive() {
  var one = document.FormName.FieldA.value.toLowerCase();
  var another = document.FormName.FieldB.value.toLowerCase();
  if (one == another) {
    return true;
  }
  alert("Oops, both fields must be identical.");
  return false;
}
```