# flumm-fetch

## Usage Example
### async / await
```javascript
import fetch from "flumm-fetch";

// GET
(async () => {
  const query = await fetch("https://example.com/file.json");
  const result = await query.json();
  console.log(result);
})();

// POST
(async () => {
  const opts = {
    method: "POST",
    body: {
      name: "John Doe",
      password: "pwd"
    }
  };
  const query = await fetch("https://example.com/file.json", opts);
  const result = await query.json();
  console.log(result);
})();
```
### promises
```javascript
import fetch from "flumm-fetch";

// GET
fetch("https://google.de")
  .then(res => res.text())
  .then(res => console.log(res))
  .catch(console.error);

// POST
const opts = {
  method: "POST",
  body: {
    name: "John Doe",
    password: "pwd"
  }
};
fetch("https://google.de", opts)
  .then(res => res.text())
  .then(res => console.log(res))
  .catch(console.error);
```

## License
This project is licensed under the MIT license, see [LICENSE](LICENSE).