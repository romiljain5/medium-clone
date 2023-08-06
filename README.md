# Medium Clone

- Checkout medium blog on vercel - https://medium-clone-k1feq3m45-jromil51-gmailcom.vercel.app 
- Build Medium blog clone with NEXT.JS, ReactJs, TypeScript, Sanity CMS, GROQ (similar to graphQL), React, Tailwind CSS, ISR((Incremental Static Regeneration)) , next-sanity, react-portable-text
- typings.d.ts file means definition typescript file, It is about how we store type definitions
- NextJs SSR -> Nextjs server prebuilds the page, /page per request
- if you visit a page which does not exist with /post/anyname then it will give 404 error
- we have used [slug].js for linking posts to page according to slugs which we get from sanity schema
- used revalidate from sanity so after 60 sec, it'll update the old cache, will delete old cache and had new one, so page can get changes automatically
    - ISR (Incremental Static Regeneration) → Next.js allows you to create or update static pages after you've built your site. Incremental Static Regeneration (ISR) enables you to use static-generation → https://nextjs.org/docs/basic-features/data-fetching/incremental-static-regeneration
    - using revalidate
- react-portable-text - An easy way to render Portable Text block content in React applications. (you cannot edit img tag in specializers)
- Used react-hook-form for form validations → [https://react-hook-form.com](https://react-hook-form.com/)
- comment will get showed only after approval of moderator

### Project Video
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/xkWIAKZOrrc/0.jpg)](https://www.youtube.com/watch?v=xkWIAKZOrrc)

### Usefull commands

- npm init
- yarn run dev (runs project)
- install sanity globally and make sanity account (npm install -g @sanity/cli)
- use (sanity init) for initializing sanity
- Starting sanity
  - cd mediumsanity
  - sanity start (starts sanity on port)
- use GROQ query language to get data from sanity in sanity studio → vision

```
*[_type == "post"]{
  _id,
  title,
  author-> {
  name,
  image
	// you can also use ... spread operator to get all things
},
description,
mainImage,
slug,
}
```

### .env.local

- Make .env.local in root folder with below details, found details from sanity.json file as projectId, dataset
- adding NEXT_PUBLIC allows access to client as well as API side

```
NEXT_PUBLIC_SANITY_DATASET=production
NEXT_PUBLIC_SANITY_PROJECT_ID=
SANITY_API_TOKEN=
```

### Tips

- Interfaces are better type, because in interface you can do extending, means you can inherit types from other types
- if you are using .then then you don’t need to use await async
- API_TOKEN_KEY allows us to read and write to database in sanity

### Usefull Links

- next-sanity → https://www.npmjs.com/package/next-sanity
- ISR (Incremental Static Regeneration) → https://nextjs.org/docs/basic-features/data-fetching/incremental-static-regeneration
- react-portable-text → https://www.npmjs.com/package/react-portable-text
