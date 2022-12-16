# animein!

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
