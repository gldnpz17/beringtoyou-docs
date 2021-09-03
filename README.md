# beringtoyou-docs
BeringToYou merupakan repositori pedagang pasar beringharjo yang berusaha membantu digitalisasi pasar beringharjo. Berikut merupakan dokumentasi REST API beringtoyou untuk mempermudah integrasi dengan sistem informasi lain.

## Mendapatkan Daftar Semua Toko
### Request
Contoh: 

`GET https://beringtoyou.com/api/shops?keywords=kerajinan+souvenir&category=a39018ee-6a0c-45b0-83a7-8c1e841c8b55&onlineshop=4c4dd6c5-35df-4cad-8682-be15c13673a9+9d043248-88e7-4222-a600-0f61ac752f6c&subcategory=481e5138-b9af-4f1f-a980-b5b1ec86ea18+f9e88359-d663-4a92-82d9-cb8a82d35d1b&minprice=1000&maxprice=20000`

#### Endpoint
`GET https://beringtoyou.com/api/shops`
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

`GET https://beringtoyou.com/api/shops/aec14246-120e-4bd5-a1d6-64c48e4a5446`
#### Endpoint
`GET https://beringtoyou.com/api/shops/{Shop ID}`

### Response
Status Code : `200 OK`

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

## Mendapatkan Semua Kategori Toko
### Request

#### Endpoint
`GET https://beringtoyou.com/api/shops/shop-categories`

### Response
Status Code: `200 OK`

```
[
  {
    "id": "b0b5308f-1cf0-4a81-b3ab-fa682500ac30",
    "name": "Sembako",
    "iconFilename": null
  },
  {
    "id": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Kerajinan",
    "iconFilename": "BFmURut8b1UJlBCaJzvm4SFlsOpuN7CPCusizFboExW0f8bKeXaLC9Ns9BlCE8ve.svg"
  },
  {
    "id": "0007cdda-5c6a-46d7-b60d-b3a44aee474c",
    "name": "Baju/Tekstil",
    "iconFilename": "epTQiuuLxIKqCrulqkdC0alKrNUkUgZSQIr5AmO8GJTBBiPFliV0dntDDIiUaK0R.svg"
  },
  {
    "id": "0434b72b-07bd-4c99-8136-ccae3bed508c",
    "name": "Makanan",
    "iconFilename": "iNQroa9xUDRLK0hHJR1s00SZNVg91sfkBQLM1imEh4WYAdhRz2l0oV5s51dT496l.svg"
  },
  {
    "id": "30caaf4a-3b6b-4c10-bd2f-4c67b6414907",
    "name": "Obat-obatan tradisional",
    "iconFilename": "J3GZeg2HC4jQcWDq5cBPp8yu9J00iBsyBYBBtMgTqXWBs3FAjlWLa4fLEVaUpCjA.svg"
  },
  {
    "id": "08773222-c418-4215-9c0d-7b8291adc881",
    "name": "Sayur dan/atau Buah",
    "iconFilename": "pnJGFt7rDrmNsHAbWxOf3sTVyYCdEYo9v7E3HjBOjuwjOrHphvoqUzx6TyRqqdno.svg"
  },
  {
    "id": "7de88470-3700-42e8-abd3-b4a416f83307",
    "name": "Ikan dan/atau daging",
    "iconFilename": "rX2VUkQv2Euii2ntNtO7LT6ZvibnAZ8UaQJn442M7T9gvcfDlUmMRq4YbckwJmvd.svg"
  }
]
```

## Mendapatkan Semua Platform Toko Online
### Request

#### Endpoint
`GET https://beringtoyou.com/api/online-shop-platforms`

### Response
Status Code: `200 OK`

```
[
  {
    "id": "4c4dd6c5-35df-4cad-8682-be15c13673a9",
    "name": "Lazada",
    "iconFilename": null
  },
  {
    "id": "3f6df5ac-4abf-45d0-8c4b-7704c5879de9",
    "name": "Tokopedia",
    "iconFilename": null
  },
  {
    "id": "399dda73-5198-4a14-8116-1a684efe4861",
    "name": "Shopee",
    "iconFilename": "74kSc5z9H8LkCHsm7AgcpdRIptrf0bZtNYGsrUdy70ncV7UQhVG6MMbenbntNTJq.png"
  },
  {
    "id": "fb1964d5-7258-424d-a636-401beac60ab7",
    "name": "Instagram",
    "iconFilename": "ru7qLJdZcK5MquiUeSYdoMXrRwq8At3FIdun2yrcl2t5yrESgTzKGekfWQYZdeZt.svg"
  },
  {
    "id": "9d043248-88e7-4222-a600-0f61ac752f6c",
    "name": "Facebook",
    "iconFilename": "X8wvNZ341vnfQtXr2NEMx64c7rtYq3qVbGyBoiWzvi12dUso92DMTmhaDUxgpeN7.png"
  },
  {
    "id": "9d61294b-f3c6-48f8-9efd-b22ce0259bf3",
    "name": "Bukalapak",
    "iconFilename": "0yxc9Y8AbRO4sDR0sBxE127rd51NB45voWnBu3fokVbWOPFuTkbClnp71F8Dgv8g.png"
  }
]
```

## Mendapatkan Subkategori dari Kategori Toko
### Request
Contoh: `GET https://beringtoyou.com/api/shops/shop-categories/a39018ee-6a0c-45b0-83a7-8c1e841c8b55/subcategories`

#### Endpoint
`GET https://beringtoyou.com/api/shops/shop-categories/{Category ID}/subcategories`

### Response
Status Code: `200 OK`

```
[
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
  },
  {
    "id": "e11e43fb-fbe7-4c07-be18-242df396c20a",
    "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Perabotan",
    "rgbHexLegendColor": "#32c115"
  },
  {
    "id": "d283f9fe-8568-465f-84e9-cda10a09f1b4",
    "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Perlengkapan Pernikahan",
    "rgbHexLegendColor": "#2d33e1"
  },
  {
    "id": "eb39467b-873b-494d-8017-357f7dcd8b3d",
    "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Jam",
    "rgbHexLegendColor": "#3781e1"
  },
  {
    "id": "e47952ce-c459-4583-bae4-29c6b0331ef3",
    "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Tas",
    "rgbHexLegendColor": "#e63d3d"
  },
  {
    "id": "55e7e063-f4a7-42bd-b9df-ec49b9f017b2",
    "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Emas dan Logam Mulia",
    "rgbHexLegendColor": "#dafb37"
  },
  {
    "id": "1413f1ea-ee68-43a4-891a-50fd45b6bb9a",
    "categoryId": "a39018ee-6a0c-45b0-83a7-8c1e841c8b55",
    "name": "Souvenir",
    "rgbHexLegendColor": "#f5c724"
  }
]
```

## Mendapatkan Semua Peta Lantai Pasar
### Request
#### Endpoint
`GET https://beringtoyou.com/api/map/floors`
### Response
Status Code: `200 OK`

```
[
  {
    "id": "c5081678-ba21-4f3f-a134-a95c83b712b1",
    "floorNumber": 1,
    "kmlFilename": "J0sIZuE2XRRVuOJLadr9eK8fi2Nd6frmkhGhHmaASQbpvgfArYB5CRv92Mkggl62.kml"
  },
  {
    "id": "61fa3d62-a6a6-4b06-8797-e7d790dd7470",
    "floorNumber": 2,
    "kmlFilename": null
  },
  {
    "id": "612bd57c-2a41-4dae-9960-cea8d38e48b9",
    "floorNumber": 3,
    "kmlFilename": null
  }
]
```

## Mendapatkan Semua Legenda Peta
### Request
#### Endpoint
`GET https://beringtoyou.com/api/map/legends`
### Response
Status Code: `200 OK`

```
[
  {
    "id": "61d9b57c-2bb1-4db7-9960-aee7d38e4ab9",
    "iconFilename": "X8wvNZ341vnfQtXr2NEMx64c7rtYq3qVbGyBoiWzvi12dUso92DMTmhaDUxgpeN7.svg",
    "label": "Jalan Utama"
  }
]
```

## Mendapatkan Semua Overlay Peta
### Request
#### Endpoint
`GET https://beringtoyou.com/api/map/overlays`
### Response
Status Code: `200 OK`

```
[
  {
    "id": "c5081678-ba21-413a-a134-a95b83b712c9",
    "floorNumber": 1,
    "zIndex": 1,
    "name": "Blok Toko",
    "iconFilename": "ru7qLJdZcK5MquiUeSYdoMXrRwq8At3FIdun2yrcl2t5yrESgTzKGekfWQYZdeZt.kml"
  }
]
```

## Mendapatkan Semua Point of Interest (Non-Toko)
### Request
#### Endpoint
`GET https://beringtoyou.com/api/map/points-of-interest`
### Response
Status Code: `200 OK`
```
[
  {
    "id": "81536229-28c3-4690-8d4c-ac93033ff792",
    "category": {
      "id": "19457d9b-b351-4b2f-8d3f-abbfeed1f3c2",
      "name": "Mushola",
      "iconFilename": "tHBLWSK0FsXoLqtF2qU24OV4RlVuWby8zFrBtV3LTR2pTV4mMXMiXGvevG4v7ado.svg"
    },
    "floorNumber": 2,
    "latitude": -7.798687,
    "longitude": 110.365753
  },
  {
    "id": "c3f11c4e-6fe8-4cd3-8cfe-0b862a230853",
    "category": {
      "id": "3fef2a2b-954f-4299-bde9-df9602eb6bcd",
      "name": "WC",
      "iconFilename": "xTwgRtcFwqjM9YBg9TsaeL2y8sEy3iJbWiRhlapeS8xbz2SrAj6dwKimb8hjpoMO.svg"
    },
    "floorNumber": 2,
    "latitude": -7.798598,
    "longitude": 110.365639
  },
  {
    "id": "9a4f6a06-7266-482d-8a13-e637545deb0e",
    "category": {
      "id": "19457d9b-b351-4b2f-8d3f-abbfeed1f3c2",
      "name": "Mushola",
      "iconFilename": "tHBLWSK0FsXoLqtF2qU24OV4RlVuWby8zFrBtV3LTR2pTV4mMXMiXGvevG4v7ado.svg"
    },
    "floorNumber": 2,
    "latitude": -7.798492,
    "longitude": 110.366341
  },
  {
    "id": "20c63d24-7754-45f4-8df3-deac0b0cd921",
    "category": {
      "id": "3fef2a2b-954f-4299-bde9-df9602eb6bcd",
      "name": "WC",
      "iconFilename": "xTwgRtcFwqjM9YBg9TsaeL2y8sEy3iJbWiRhlapeS8xbz2SrAj6dwKimb8hjpoMO.svg"
    },
    "floorNumber": 1,
    "latitude": -7.798492,
    "longitude": 110.366341
  },
  {
    "id": "f931afc2-c6a0-45a1-bbf3-924b720ec4b0",
    "category": {
      "id": "2113aac6-d8f1-487d-8ba8-88f8f9ba4b8d",
      "name": "Foodcourt/Kantin",
      "iconFilename": "4nnzIiAe9Qno0C9hLX6W7ZqGyrbhaLI3tNHLfx3yPY42qvql5jWFlYyf7gAbHdEy.svg"
    },
    "floorNumber": 2,
    "latitude": -7.798783,
    "longitude": 110.366707
  },
  {
    "id": "857b5d66-e995-436a-9017-3b40d518e786",
    "category": {
      "id": "a935dbb4-7fd2-4f28-a948-cf9a18f2e1eb",
      "name": "ATM Mandiri",
      "iconFilename": "JlTndbFz3sDGPdaCdgeJqGtVpiDQoMa7JdlMrQ9SKLq2TVxMCQrMQrvD2774XyLr.svg"
    },
    "floorNumber": 2,
    "latitude": -7.798877,
    "longitude": 110.36644
  }
]
```

## Mendapatkan Semua Kategori Point of Interest (Non-Toko)
### Request
#### Endpoint
`GET https://beringtoyou.com/api/map/point-of-interest-categories`
### Response
Status Code: `200 OK`
```
[
  {
    "id": "3fef2a2b-954f-4299-bde9-df9602eb6bcd",
    "name": "WC",
    "iconFilename": "xTwgRtcFwqjM9YBg9TsaeL2y8sEy3iJbWiRhlapeS8xbz2SrAj6dwKimb8hjpoMO.svg"
  },
  {
    "id": "19457d9b-b351-4b2f-8d3f-abbfeed1f3c2",
    "name": "Mushola",
    "iconFilename": "tHBLWSK0FsXoLqtF2qU24OV4RlVuWby8zFrBtV3LTR2pTV4mMXMiXGvevG4v7ado.svg"
  },
  {
    "id": "2113aac6-d8f1-487d-8ba8-88f8f9ba4b8d",
    "name": "Foodcourt/Kantin",
    "iconFilename": "4nnzIiAe9Qno0C9hLX6W7ZqGyrbhaLI3tNHLfx3yPY42qvql5jWFlYyf7gAbHdEy.svg"
  },
  {
    "id": "a935dbb4-7fd2-4f28-a948-cf9a18f2e1eb",
    "name": "ATM Mandiri",
    "iconFilename": "JlTndbFz3sDGPdaCdgeJqGtVpiDQoMa7JdlMrQ9SKLq2TVxMCQrMQrvD2774XyLr.svg"
  }
]
```

## Mendapatkan Asset Publik
### Request
Contoh:

`GET https://beringtoyou.com/api/public/assets/lIB87HUxushn63a1PtKyK4qh9oYg05I2IBw9Rkhdq7S1XdzvhzQPmgMqce9Stx7z.jpg`
#### URL
`GET https://beringtoyou.com/api/public/assets/{Filename}`

### Response
Status Code: `200 OK`

Body berisi konten file yang di-request.
