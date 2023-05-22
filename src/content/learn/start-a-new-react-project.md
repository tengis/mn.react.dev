---
title: Шинэ React төсөл эхлүүлэх
---

<Intro>

Хэрэв та React ашиглан шинэ апп эсвэл шинэ вебсайт бүтээхийг хүсвэл, бид танд React дээр суурилсан түгээмэл ашиглагддаг фраймворкуудаас нэгийг сонгохыг санал болгож байна. Учир нь тухайн фраймворкууд ихэнхи апп болон вебүүдэд эцсийн дүнд хэрэг болдог боломжуудыг өөртөө агуулсан байдаг бөгөөд үүнд routing, data fetching and HTML автоматаар үүсгэх гэх мэт багтсан байдаг.

</Intro>

<Note>

**Local хөгжүүлэлт хийхийн тулд та [Node.js](https://nodejs.org/en/) суулгах шаардлагатай** бөгөөд түүгээр ч зогсохгүй та Node.js -г Production -нд ашиглах боломжтой. Гэвч хэрвээ хүсвэл ашиглахгүй байж болно. Учир нь олонхи React -д суурилсан фраймворкууд static HTML/CSS/JS байрлах хавтас дэмждэг.

</Note>

## Production шаардлага хангасан React фрэймворкууд {/*production-grade-react-frameworks*/}

### Next.js {/*nextjs*/}

**[Next.js](https://nextjs.org/) бол шалгарсан full-stack React фрэймворк юм.** Уг фрэймворкоор та энгийн static блогоос эхлээд маш өргөн боломжтой олон төрлийн динамик функцтэй апп хийх боломжтой. Хэрэв Next.js -г ашиглан шинэ апп эхлүүлэхийн тулд та терминал дээр дараах коммандыг ажиллуулна:

<TerminalBlock>
npx create-next-app
</TerminalBlock>

Хэрэв та Next.js -г анхлан ашиглаж байгаа бол дараахи [Next.js хичээл](https://nextjs.org/learn/basics/create-nextjs-app) -г үзээрэй.

Next.js -г [Vercel](https://vercel.com/) хөгжүүлдэг ба та өөрийн [Next.js дээр хөгжүүлэгдсэн аппликэшнээ](https://nextjs.org/docs/deployment) ямар ч төрлийн Node.js эсвэл serverless хостинг, эсвэл өөрийнхөө сервер дээр ч deploy хийж болох юм. Түүнчлэн та [бүрэн static Next.js апп хөгжүүлж буй бол](https://nextjs.org/docs/advanced-features/static-html-export) үүнийгээ бүх төрлийн static хостинг рүү deploy хийж болно.

### Remix {/*remix*/}

**[Remix](https://remix.run/) бол агуулагдсан (nested) routing -тэй full-stack React фрэймворк юм.** Уг фрэймворкыг ашиглан өөрийн аппыг өөр дотороо агуулагдсан хэсгүүдэд хуваан хөгжүүлж болох ба тухайн хэсгүүд тус тусдаа нэгэн зэрэг өгөгдөл ачаалах бас хэрэглэгчийн action -д үр дүнг үзүүлэх боломжтой юм. Хэрэв та Remix -г ашиглан шинэ апп эхлүүлэхийн тулд та терминал дээр дараах коммандыг ажиллуулна:

<TerminalBlock>
npx create-remix
</TerminalBlock>

Хэрэв та Remix -г анхлан ашиглаж байгаа бол дараахи [Remix хичээл](https://remix.run/docs/en/main/tutorials/blog) (богино) -г болон [апп хийх хичээл](https://remix.run/docs/en/main/tutorials/jokes) (урт) үзээрэй.

Remix -г [Shopify](https://www.shopify.com/) хөгжүүлдэг ба Remix дээр төсөл үүсгэхдээ та [хаана deploy](https://remix.run/docs/en/main/guides/deployment) хийхээ сонгох хэрэгтэй. Мөн түүнчлэн та дурын Node.js эсвэл serverless хостинг рүү Remix аппликэшнээ [adapter](https://remix.run/docs/en/main/other-api/adapter) ашиглаж эсвэл бичиж deploy хийж болно.

### Gatsby {/*gatsby*/}

**[Gatsby](https://www.gatsbyjs.com/) fast CMS тэй веб сайтуудад зориулагдсан React дээр суурилсан фрэймворк юм.** Уг фрэймворк нь маш сайн нэмэлтүүдтэй ба GraphQL суурилсан энгийн контент layer, API -ууд болон services гэх мэтийг ашиглан веб хийх явцыг хялбарчилдэг. Хэрэв та Gatsby -г ашиглан шинэ апп эхлүүлэхийн тулд та терминал дээр дараах коммандыг ажиллуулна:

<TerminalBlock>
npx create-gatsby
</TerminalBlock>

Хэрэв та Gatsby -г анхлан ашиглаж байгаа бол дараахи [Gatsby хичээл](https://www.gatsbyjs.com/docs/tutorial/) -г үзээрэй.

Gatsby -г [Netlify](https://www.netlify.com/) хөгжүүлдэг. Та [бүрэн static Gatsby сайт](https://www.gatsbyjs.com/docs/how-to/previews-deploys-hosting) -г аль ч static хостинг рүү deploy хийж болно. Хэрвээ та server-only features ашиглахыг сонгосон бол таны хостинг server-only features -г дэмжих эсэхийг шалгана уу.

### Expo (for native apps) {/*expo*/}

**[Expo](https://expo.dev/) -г ашиглан та Android, iOS болон веб дээр native UI -тэй universal апп хийх боломжтой.** Expo нь өөртөө React Native -д зориулсан SDK агуулдаг ба энэ нь native UI хэсгүүдийг хийхэд хялбархан болгож өгдөг. Шинэ Expo төсөл үүсгэхийн тулд та терминал дээр дараах коммандыг ажиллуулна:

<TerminalBlock>
npx create-expo-app
</TerminalBlock>

Хэрвээ та Expo -г анхлан ашиглаж байгаа бол дараахи [Expo хичээл](https://docs.expo.dev/tutorial/introduction/) -г үзээрэй.

Expo -г [Expo (the company)](https://expo.dev/about) хөгжүүлдэг. Expo -г ашиглан апп хийх нь үнэгүй бөгөөд та түүнийг Google болон Apple app store дээр ямар нэгэн хязгаарлалтгүйгээр гаргаж болно. Мөн түүнчлэн Expo нь нэмэлтээр төлбөртэй cloud service -үүдийг санал болгодог.

<DeepDive>

#### Би React -г ямар нэгэн фрэймфоркгүйгээр ашиглах боломжтой юу? {/*can-i-use-react-without-a-framework*/}

Мэдээж хэрэг та React -г ямар нэгэн фрэймфорк ашиглахгүйгээр ашиглаж болно -- [энд хэрхэн React -г таны вэб сайтын нэг хэсэгт ашиглахыг харуулсан байна.](/learn/add-react-to-an-existing-project#using-react-for-a-part-of-your-existing-page) **Гэхдээ бид танд шинэ апп эсвэл вебсайт бүтээхийн тулд фрэймфорк ашиглахыг санал болгож байна.**


Яагаад вэ гэвэл.

Even if you don't need routing or data fetching at first, you'll likely want to add some libraries for them. As your JavaScript bundle grows with every new feature, you might have to figure out how to split code for every route individually. As your data fetching needs get more complex, you are likely to encounter server-client network waterfalls that make your app feel very slow. As your audience includes more users with poor network conditions and low-end devices, you might need to generate HTML from your components to display content early--either on the server, or during the build time. Changing your setup to run some of your code on the server or during the build can be very tricky.

**These problems are not React-specific. This is why Svelte has SvelteKit, Vue has Nuxt, and so on.** To solve these problems on your own, you'll need to integrate your bundler with your router and with your data fetching library. It's not hard to get an initial setup working, but there are a lot of subtleties involved in making an app that loads quickly even as it grows over time. You'll want to send down the minimal amount of app code but do so in a single client–server roundtrip, in parallel with any data required for the page. You'll likely want the page to be interactive before your JavaScript code even runs, to support progressive enhancement. You may want to generate a folder of fully static HTML files for your marketing pages that can be hosted anywhere and still work with JavaScript disabled. Building these capabilities yourself takes real work.

**React frameworks on this page solve problems like these by default, with no extra work from your side.** They let you start very lean and then scale your app with your needs. Each React framework has a community, so finding answers to questions and upgrading tooling is easier. Frameworks also give structure to your code, helping you and others retain context and skills between different projects. Conversely, with a custom setup it's easier to get stuck on unsupported dependency versions, and you'll essentially end up creating your own framework—albeit one with no community or upgrade path (and if it's anything like the ones we've made in the past, more haphazardly designed).

If you're still not convinced, or your app has unusual constraints not served well by these frameworks and you'd like to roll your own custom setup, we can't stop you--go for it! Grab `react` and `react-dom` from npm, set up your custom build process with a bundler like [Vite](https://vitejs.dev/) or [Parcel](https://parceljs.org/), and add other tools as you need them for routing, static generation or server-side rendering, and more.
</DeepDive>

## Bleeding-edge React frameworks {/*bleeding-edge-react-frameworks*/}

As we've explored how to continue improving React, we realized that integrating React more closely with frameworks (specifically, with routing, bundling, and server technologies) is our biggest opportunity to help React users build better apps. The Next.js team has agreed to collaborate with us in researching, developing, integrating, and testing framework-agnostic bleeding-edge React features like [React Server Components.](/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023#react-server-components)

These features are getting closer to being production-ready every day, and we've been in talks with other bundler and framework developers about integrating them. Our hope is that in a year or two, all frameworks listed on this page will have full support for these features. (If you're a framework author interested in partnering with us to experiment with these features, please let us know!)

### Next.js (App Router) {/*nextjs-app-router*/}

**[Next.js's App Router](https://beta.nextjs.org/docs/getting-started) is a redesign of the Next.js APIs aiming to fulfill the React team’s full-stack architecture vision.** It lets you fetch data in asynchronous components that run on the server or even during the build.

Next.js is maintained by [Vercel](https://vercel.com/). You can [deploy a Next.js app](https://nextjs.org/docs/deployment) to any Node.js or serverless hosting, or to your own server. Next.js also supports [static export](https://beta.nextjs.org/docs/configuring/static-export) which doesn't require a server.
<Pitfall>

Next.js's App Router is **currently in beta and is not yet recommended for production** (as of Mar 2023). To experiment with it in an existing Next.js project, [follow this incremental migration guide](https://beta.nextjs.org/docs/upgrade-guide#migrating-from-pages-to-app).

</Pitfall>

<DeepDive>

#### Which features make up the React team’s full-stack architecture vision? {/*which-features-make-up-the-react-teams-full-stack-architecture-vision*/}

Next.js's App Router bundler fully implements the official [React Server Components specification](https://github.com/reactjs/rfcs/blob/main/text/0188-server-components.md). This lets you mix build-time, server-only, and interactive components in a single React tree.

For example, you can write a server-only React component as an `async` function that reads from a database or from a file. Then you can pass data down from it to your interactive components:

```js
// This component runs *only* on the server (or during the build).
async function Talks({ confId }) {
  // 1. You're on the server, so you can talk to your data layer. API endpoint not required.
  const talks = await db.Talks.findAll({ confId });

  // 2. Add any amount of rendering logic. It won't make your JavaScript bundle larger.
  const videos = talks.map(talk => talk.video);

  // 3. Pass the data down to the components that will run in the browser.
  return <SearchableVideoList videos={videos} />;
}
```

Next.js's App Router also integrates [data fetching with Suspense](/blog/2022/03/29/react-v18#suspense-in-data-frameworks). This lets you specify a loading state (like a skeleton placeholder) for different parts of your user interface directly in your React tree:

```js
<Suspense fallback={<TalksLoading />}>
  <Talks confId={conf.id} />
</Suspense>
```

Server Components and Suspense are React features rather than Next.js features. However, adopting them at the framework level requires buy-in and non-trivial implementation work. At the moment, the Next.js App Router is the most complete implementation. The React team is working with bundler developers to make these features easier to implement in the next generation of frameworks.

</DeepDive>
