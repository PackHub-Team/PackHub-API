<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="packhub_api.png">
    <img src="packhub_api.png" alt="Logo" width="512">
  </a>

<h3 align="center">PackHub API</h3>

  <p align="center">
    The PackHub API and how to use it.
    <br />
    <br />
    <a href="https://github.com/PackHub-Team/PackHub-API/tree/main/docs">Documentation</a>
    ·
    <a href="https://packhub.net">Website</a>
  </p>
</div>

<!-- ABOUT THE PROJECT -->
## Features

- Search for packs by tags, or name.
- Look at what packs people have purchased
- Download packs directly (Applicable to free packs only)
- Search for pack creators.
- Get exclusive packs.
- Get raw pack data for your own needs.

<p align="right">(<a href="#top">back to top</a>)</p>

## Valid Requests

- `../search/<query>` Returns search results from provided search query [[read more]]()
- `../pack/<id>` Returns pack data for a pack by a provided ID [[read more]]()
- `../packs/<recent|popular|exclusive>`
- `../versions`
- `../tags`
- `../status` Returns service statuses [[read more]]()

<p align="right">(<a href="#top">back to top</a>)</p>
