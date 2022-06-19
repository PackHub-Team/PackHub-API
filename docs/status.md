<!-- PROJECT LOGO -->
<br />
<div align="center">
<h1 align="center">PackHub API</h1>

  <p align="center">
  <h4>Server status</h4>
    <br />
    <a href="https://github.com/PackHub-Team/PackHub-API/">Main Page</a>
    ·
    <a href="https://packhub.net">Website</a>
  </p>
</div>

### Making a request

When using the PackHub API, you may want to check on the server status before doing anything.

Simply fetch the **root directory** of the API (or `../status`)

```javascript
fetch('https://api.packhub.net/)
  .then(res -> console.log);
```

### The response

The response will give a status on the PackHub API itself, the PackHub Website and the PackHub Discord bot.

The format of which will look like this:

```json
{
  "api": {
    "status": "OKAY",
    "uptime": 1273972193,
    "requests": 12343,
    "rps": 0
  },
  "website": {
    "status": "OKAY",
    "uptime": 178278,
    "requests": 932,
    "rps": 0
  },
  "discord": {
    "status": "OKAY",
    "uptime": 91292,
    "requests": 932933,
    "rps": 1
  }
}
```

The `status` will return `"UNAVAILABLE"`, `"PARTIAL"` or `"OKAY"`.

Data Types:
- `status`: enum(`"UNAVAILABLE" | "PARTIAL" | "OKAY"`)
- `uptime`: long
- `requests`: long
- `rps`: float

<p align="right">(<a href="#top">back to top</a>)</p>
