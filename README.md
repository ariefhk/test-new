# BCR API

Di dalam repository ini terdapat implementasi API dari Binar Car Rental.
Tugas kalian disini adalah:

1. Fork repository
2. Tulis unit test di dalam repository ini menggunakan `jest`.
3. Coverage minimal 70%

Good luck!

# Note Deploy Berhasil

1. Buat file Procfile di root folder diisi kaya gini gais

```Procfile
web: npm start
release: npm run db:migrate && npm run db:seed
```

2. open project > config > database.js
3. edit import env

```js
// INI DICOMMENT AJA
// const {
//   DB_USER = "",
//   DB_PASSWORD = "",
//   DB_NAME = "bcr",
//   DB_HOST = "127.0.0.1",
//   DB_PORT = "5432",
// } = process.env;

const { DB_USER, DB_PASSWORD, DB_NAME, DB_HOST, DB_PORT } = process.env;
```

4. edit juga di module.exports dibagian production jadi kaya gini gais

```js
 production: {
        username: DB_USER,
        password: DB_PASSWORD,
        database: DB_NAME,
        host: DB_HOST, //jgn pake ${DB_HOST}_productions
        port: DB_PORT,
        dialect: "postgres",
    },
```
