# beringtoyou-docs

## Mendapatkan Daftar Semua Toko
### Request
Contoh: 

`GET https://beringtoyou.com/api/shops?keywords=kerajinan+souvenir&category=a39018ee-6a0c-45b0-83a7-8c1e841c8b55&onlineshop=4c4dd6c5-35df-4cad-8682-be15c13673a9+9d043248-88e7-4222-a600-0f61ac752f6c&subcategory=4c4ee7c5-6a0c-45b0-83a7-8c1e841c8b55+a39018ee-4cad-45b0-4cad-8c1e841c8b95&minprice=1000&maxprice=20000`

#### URL
`GET` https://beringtoyou.com/api/shops
#### Query String Parameters
* `keywords`: Daftar kata kunci pencarian.
* `category`: ID kategori toko.
* `subcategory`: Daftar ID subkategori.
* `onlineshop`: Daftar ID toko online.
* `minprice`: Harga minimum berupa `integer`.
* `maxprice`: Harga maximum berupa `integer`.
* `start`: Ambil mulai toko yang disebutkan dalam parameter ini. (e.g. ambil mulai toko ke-5)
* `count`: Jumlah toko yang diambil.

### Response
Status code: `200 OK`

```
[
  {
    "id": "b0e548c3-e6c6-4e18-84c2-d3184bae6a4a",
    "name": "Ibu Wasilah Dompet Kipas Souvenir",
    "bannerImage": {
      "filename": "1bjcEYG5uVCRDpLBu2ta7zhPaLAVj2TToLgtboflqV6lnBU2vuebtneB4UC2YuV2.jpg",
      "thumbnailFilename": "OeFDCTYcz8znxaG5GDmZhrMOkM4ibVY0spaRYi4AtDbkJCfFXuIG9WBgS0c0Z0Bd.jpg"
    },
    "floor": 1,
    "latitude": -7.799087,
    "longitude": 110.366531,
    "shopCategoryName": "Kerajinan",
    "subcategories": [],
    "category": {
      "id": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
      "name": "Kerajinan",
      "iconFilename": "BFmURut8b1UJlBCaJzvm4SFlsOpuN7CPCusizFboExW0f8bKeXaLC9Ns9BlCE8ve.svg",
    }
  },
  {
    "id": "4340e717-9c98-4bba-abc0-ae8be517b448",
    "name": "Novan Souvenir",
    "bannerImage": {
      "filename": "abrH83VAYLbywaPXKtpHa0kc2OjedRCnhf0WgdbHZFJFDe5geIQEvG3j1PPuU1gH.jpg",
      "thumbnailFilename": "dreOFbaKuorCXMCdlwpJKlfg8YgUyRo7PfU9Q2l1F6bBzVNPNdpY4bL2M8Pr4FVd.jpg"
    },
    "floor": 1,
    "latitude": -7.79853,
    "longitude": 110.36715,
    "shopCategoryName": "Kerajinan",
    "subcategories": [],
    "category": {
      "id": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
      "name": "Kerajinan",
      "iconFilename": "BFmURut8b1UJlBCaJzvm4SFlsOpuN7CPCusizFboExW0f8bKeXaLC9Ns9BlCE8ve.svg",
    }
  }
]
```

## Mendapatkan Detail Toko
### Request
Contoh:

`https://beringtoyou.com/api/shops/aec14246-120e-4bd5-a1d6-64c48e4a5446`
#### URL
`GET https://beringtoyou.com/api/shops/{Shop ID}`

### Response
```
{
  "id": "aec14246-120e-4bd5-a1d6-64c48e4a5446",
  "name": "Lestari Accessoris",
  "bannerImage": {
    "filename": "a941N7vx5gJoSOM9QMYgP97FZi78i5NZUkDo8G09mDW4En9Ndl7P5k2bBzcp9wP9.jpg",
    "thumbnailFilename": "w14FTN8mhr2ko6Lwz6kZPJ8a2260r9r9tNlujahKeQX5qKu4Zpox9ulm3dMbRI5i.jpg"
  },
  "ownerNames": ["Lestari"],
  "description": "Pasar Beringharjo Lantai 1 Blok D Los 8 sebelah selatan",
  "floor": 1,
  "latitude": -7.799153,
  "longitude": 110.366852,
  "category": {
    "id": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Kerajinan",
    "iconFilename": "BFmURut8b1UJlBCaJzvm4SFlsOpuN7CPCusizFboExW0f8bKeXaLC9Ns9BlCE8ve.svg",
  },
  "subcategories": [
    {
      "id": "481e5138-b9af-4f1f-a980-b5b1ec86ea18",
      "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
      "name": "Aksesoris",
      "rgbHexLegendColor": "#e63392"
    },
    {
      "id": "f9e88359-d663-4a92-82d9-cb8a82d35d1b",
      "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
      "name": "Craft",
      "rgbHexLegendColor": "#aa2dd7"
    }
  ],
  "onlineShopInstances": [
    {
      "id": "884a5efd-4946-45b2-addf-6fb7f2788f79",
      "platform": {
        "id": "fb1964d5-7258-424d-a636-401beac60ab7",
        "name": "Instagram",
        "iconFilename": "ru7qLJdZcK5MquiUeSYdoMXrRwq8At3FIdun2yrcl2t5yrESgTzKGekfWQYZdeZt.svg"
      },
      "name": " kranon.acc",
      "url": "https://www.instagram.com/kranon.acc/"
    },
    {
      "id": "d433fd1d-3bff-4669-abce-3fc0fc48ff81",
      "platform": {
        "id": "399dda73-5198-4a14-8116-1a684efe4861",
        "name": "Shopee",
        "iconFilename": "74kSc5z9H8LkCHsm7AgcpdRIptrf0bZtNYGsrUdy70ncV7UQhVG6MMbenbntNTJq.png"
      },
      "name": "sayidrisq",
      "url": "https://shopee.co.id/sayidrisqi"
    },
    {
      "id": "3699792a-b0cf-42a5-8381-0acdd9b19778",
      "platform": {
        "id": "9d61294b-f3c6-48f8-9efd-b22ce0259bf3",
        "name": "Bukalapak",
        "iconFilename": "0yxc9Y8AbRO4sDR0sBxE127rd51NB45voWnBu3fokVbWOPFuTkbClnp71F8Dgv8g.png"
      },
      "name": "FLS Shop",
      "url": "https://www.bukalapak.com/u/syayid_risqi_yanto?from=omnisearch&from_keyword_history=false&search_source=omnisearch_user&source=navbar"
    }
  ],
  "minPrice": 1000,
  "maxPrice": 250000,
  "shopOwners": [],
  "whatsappContacts": [
    {
      "id": "4a173688-2da8-46bd-ac7f-67d837d551b5",
      "contactIdentity": "+62 856-4374-4333",
      "contactUrl": "https://wa.me/6285643744333"
    }
  ]
}
```
