
# SSG: Static Site Generation

### Definition and use:
- Creating website (Natively without using any framework), stored on the server, when user visits the website, the server sends the HTML to the browser to render it.

### Why creating static websites in first place?
- It's more optimized according to the seo engines which improves the website overall accessibilities, performance.

### Drawback of static site generation:
- If there is a link between the website and an external database, it won't get autmatically updated when there are new updates.

### Examples of static site generation projects:
- Portofolios, landing pages, forms, etc....

<hr>

# CSR: Client Site Rendering

### Definition and use:
- Creating website using frameworks like(React - Angular - Vue, etc..) that supports SPA(Single Page application)
- When you uploud the website on the server, the website has html tags but doesn't have data inside of it, for example in React(there is a div named root) and the website is rendered after executing the javascript code inside of it and later we can interact with the website and do crud operations.

### Drawback of Client Site Rendering:

- Seo poor results, the website doesn't get properly archived becasue the whole website is based on javascript, for example in Reac (It's based on components architecture that's based on javascript).
- Google site crawlers archive the browsers usig metatags like titles, headings, etc..
- (CSR) doesn't offer metatags, Google is currently working on enhacning their site crawlers to detect javascript more effiencetly.
- If the bundle size of the website is too large or it's a big project with numerous files, the website is gonna take sometime to be rendered.

<hr>

# SSR: Server Side Rendering

### Definition and use:
- Using backend languages and uplouding the website on the server, so any link between the website and the database all of this happens inside the server, then when user visits the website, the whole website is sent to the browser(Has good seo performance), Example( Next.Js)

<hr>

# ISR: Incremental Static Regeneration

### Definition and use:
- Similar to SSG, in the production phase and making the build folder, by using the (ISR) the project is uploud on host server like (Vercel), when user enters the website, it's rendered in a high speed with a good seo performance. The browser and database still have a connection between them, whem the website is loaded, we do something called re-validate, that basically checks if there are anu updates happened to update the data on the website by removing the old data and entering the news ones with the new values that exists on both the server adn the browser

# What does Next.Js offers?

- Documentaion link [Next.Js](https://nextjs.org/)
1.  Image Optimization
2.  Internationalization
3.  Next.Js analytics
4.  Zero Config
5.  Hybrid: SSG and SSR
6.  Incremental Static Regeneration
7.  TypeScript Support
8.  Fast Refresh
9.  File-system Routing
10. Api routes
11. Built-in CSS Support
12. Code-splitting and bundling

<hr>

### Reference:

- Video-link [Difference between SSR, CSR, SSG and ISR](https://youtu.be/kL6KVTHtW-s)
