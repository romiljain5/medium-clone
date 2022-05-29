# Medium Clone
- Build Medium blog clone with NEXT.JS, ReactJs, TypeScript, Sanity CMS, GROQ (similar to graphQL), React, Tailwind CSS, ISR, next-sanity

### Usefull commands
- npm init
- yarn run dev (runs project)
- install sanity globally and make sanity account (npm install -g @sanity/cli)
- use (sanity init) for initializing sanity
- Starting sanity
    - cd mediumsanity
    - sanity start  (starts sanity on port)

### .env.local
- Make .env.local in root folder with below details, found details from sanity.json file as projectId, dataset
- adding NEXT_PUBLIC allows access to client as well as API side
```
NEXT_PUBLIC_SANITY_DATASET=production
NEXT_PUBLIC_SANITY_PROJECT=
SANITY_API_TOKEN=
```

### Usefull Links
- next-sanity → https://www.npmjs.com/package/next-sanity