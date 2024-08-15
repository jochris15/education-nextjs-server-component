# NextJS Server Component & Action

## Why use server side rendering
[Dokumentasi benefit SSR](https://nextjs.org/docs/app/building-your-application/rendering/server-components#benefits-of-server-rendering)

- Data fetching
- Security 
- Performance 
- SEO & Social network shareability 
- Streaming

## Directive
[Dokumentasi directive](https://react.dev/reference/rsc/directives)

By default, NextJS menggunakan SSR. Jika ingin melakukan rendering secara CSR, gunakan 'use client' di filenya.
<br>
<br>
Jika ingin merender secara CSR, kita harus mengubah kodingan kita seperti menggunakan react. By default ada react strict mode. Jika ingin mengubah , bisa edit di next.config.mjs
<br>
<br>
Cara rendering juga bisa dicampur, jika kita menginginkan component tersebut interaktif, kita harus menggunakan CSR , contoh : di product card kita ingin ada onClick (event interaktif, di server gabisa), maka kita bisa merender product card secara client, tetapi fetch datanya tetap secara server

## When to use server and client components?
**Server**
- fetch data 
- jika mau akses data backend secara langsung
- jika mau menyimpan data sensitive (api key, etc)
- jika mau menyimpan dependencies besar

**Client**
- jika butuh interaktif & event listener
- jika butuh menggunakan hooks / custom hooks / lifecyle react 
- jika sedang menggunakan api browser
- jika ingin menggunakan class component react