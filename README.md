# animein!
<p align="center">
<a target="_blank" href="https://github.com/wffzy"><img src="https://dthezntil550i.cloudfront.net/bh/latest/bh1908311051118140005937162/1280_960/2340e625-0f0e-4a48-a0fe-da83b29c1f22.png" alt="" width="169" /></a>
</p>
<p align="center">
<a target="_blank" href="https://github.com/wffzy"><img title="Author" src="https://img.shields.io/badge/Author-Ditzzy-red.svg?style=for-the-badge&logo=github" /></a>
<br>
<a target="_blank" href="//npmjs.com/animein"><img src="https://img.shields.io/npm/dw/animein?color=yellow&label=Downloads&logo=npm&style=flat"></a>
<br>
<a target="_blank" href="https://www.npmjs.com/package/animein?activeTab=versions"><img src="https://img.shields.io/npm/v/animein?color=green&label=version&logo=npm&style=social"></a>
</p>


Ubah gambar Anda menerapkan gaya anime / manga menggunakan AI.

Requests Dari  [Photo2Cartoon](https://h5.tu.qq.com/web/ai-2d/cartoon/index) repository
## Installation
```bash
npm i git+github.com/wffzy/animein
```

<center>
<b>OR</b>
</center>

```bash
npm i animein
```
## IMPORTANT
Create file with name .env and fill with

```env
process.env.PROXY_IP=<Your Proxy IP>
process.env.PROXY_PORT=<Your Proxy Port>

```
Please use proxy socks5 from chinese


## Example


Mengubah gambar dari url eksternal

```js
const anime = require('animein');
anime.transform({
    photo: 'https://media.gq.com.mx/photos/5e220ec2ffa8c7000803441e/16:9/w_1920,c_limit/40-datos-curiosos-para-descubrir-a-scarlett-johansson.jpg',
    // Menyimpan gambar ke path tertentu
    destinyFolder: './images'
})
.then(data => {
    console.log('Image', data);
})
.catch(err => {
    console.log('Error', err);
});

```

Mengubah Gambar lokal menjadi base64

```js
const anime = require('animein');
const path = require('path');

anime.transform({
    photo: path.join(__dirname, './image.jpg')
})
.then(data => {
    console.log('Image in base64', data);
})
.catch(err => {
    console.log('Error', err);
});

```

Result
```js
{
    "base64": "/9j/2wBDAAYEBQYFBAYGBQYHBwYIChAKCgkJChQODww...", // Gambar dalam base64
    "url": "https://act-artifacts.shadowcv.qq.com/mqq/ai_painting_anime/res/f812533e4d2e197fecaa91c5bf1f89d_244kg.jpg",
    "all": {
    ....
    }
}
```
## Related

Anda Dapat Menggu akan whatsapp bot untuk menguah nya : [AnimeIn Bot](https://github.com/wffzy/animeinbot) [COMING SOON]
