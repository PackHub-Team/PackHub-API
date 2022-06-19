<br />
<div align="center">
<h1 align="center">PackHub API</h1>

  <p align="center">
  <h4>Search Request</h4>
    <br />
    <a href="https://github.com/PackHub-Team/PackHub-API/">Main Page</a>
    ·
    <a href="https://packhub.net">Website</a>
  </p>
</div>

### Searching

When we search, we make a request to the URL `http://192.168.1.132:9001/search/`.

We need to make sure we provide a valid **query**.

A valid query will be anything over 3 characters, which are all alphanumeric (or spaces).

We also **need** to provide a category to search in. If we do not then we will receive an error:

> e.g: We use `http://api.packhub.net/search/matte`
> 
> Response:
>
> ```json
> {"error":"CategoryError","message":"You must provide a valid category: [all|packs|pack_makers]"}
> ```

Valid `category` options are `packs`, `all` and `pack_makers`.

> A valid basic URL should look like this:
>
> `http://api.packhub.net/search/Matte?category=packs`
>
> Response:
> 
> ```json
> [
>    {
>        "id": 1,
>        "name": "Matte Dream",
>        "description": "Dark themed pack.\r\nCreated for discord.gg/packs\r\nNow public!",
>        "maker": 0,
>        "previews": "[\"https://i.imgur.com/ja2W2Zf.png\"]",
>        "icon": "https://i.imgur.com/mTwH3Cd.png",
>        "price": null,
>        "downloads": 124421241,
>        "public": true,
>        "tags": "[\"Black\",\"Modern\",\"Dark\"]",
>        "version": "1.17.1",
>        "createdAt": null,
>        "updatedAt": null
>    },
>    [...]
> ]
> ```

### Search options

- `tags=[tags seperated by ,]` - Will search for packs with these tags.
- `sortBy=[date_newest|date_oldest]` - Defaults to relevancy.
- `version=[version]` - A list of valid versions to search with can be found [here]().
- `freeOnly=[true|false]` - Only search for packs that are free.

With all these options combined together we can refine a search!

e.g with additional options: `http://api.packhub.net/search/Matte?category=packs&version=1.17.1&sortBy=ascending`


### The response
