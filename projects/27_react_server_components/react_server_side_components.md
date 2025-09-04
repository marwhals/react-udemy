# React Server components notes

---

## React Features you might not be able to use

- React Server Components (RSC)
- Server Actions
- use() with Promises

  - Important
    - Special project setup required!
    - Not supported by "standard" React project (e.g created via Vite)

---

## Why a special setup is needed

- Some features require a server-side environment
  - Code therefore must be split (by the build process / code bundler process)
  - Client side code - Executed on the client-side like most REact projects such as those created using Vite
  - Non Client-side Code - executed on server-side (or during build process) - Special project setup required

[//]: # (TODO Consider doing this if react server side is required)