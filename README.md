# Medium Clone

- Build Medium blog clone with NEXT.JS, ReactJs, TypeScript, Sanity CMS, GROQ (similar to graphQL), React, Tailwind CSS, ISR, next-sanity

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

- Interfaces are better the type, becoz in interface you can do extending, means you can inherit types from other types
- typings.d.ts file means definition typescript file, It is about how we store type definitions
- NextJs SSR -> Nextjs server prebuilds the page, /page per request
- if you visit a page which does not exist with /post/anyname then it will give 404 error
- we have used [slug].js for linking posts to page according to slugs which we get from sanity schema
- used revalidate from sanity so after 60 sec, it'll update the old cache, will delete old cache and had new one, so page can get changes automatically


### Usefull Links

- next-sanity → https://www.npmjs.com/package/next-sanity
