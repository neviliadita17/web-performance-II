# FCP (First Contenful Paint)

FCP metric measures the time from when the user first navigated to the page to when any part of the page’s content is rendered on the screen

# LCP (Largest Contenful Paint)

LCP metric report the render time of the largest image or text block visible within the viewport, relative to when the user first navigate to the page

# CLS (Cumulative Layout Shift)

CLS is a measure of the largest burst of *layout shift scores* for every [unexpected](https://web.dev/articles/cls#expected_vs_unexpected_layout_shifts) layout shift that occurs during the entire lifespan of a page.

# Testing tools

- Google PageSpeed Insights (https://pagespeed.web.dev/)
- WebPageTest (https://www.webpagetest.org/)
- GT Metrix (https://gtmetrix.com/)
- Chrome Lighthouse (Extension)


## --------------------------------------------------------------

**Untuk delay hydration (tambahkan ke project)**

    npm i -D nuxt-delay-hydration
  
**Add** di nuxt.config.ts :

```
modules: [
    'nuxt-delay-hydration'
  ],
```

```
delayHydration: {
// enables nuxt-delay-hydration in dev mode for testing
// NOTE: you should disable this once you've finished testing, it will break HMR
debug: process.env.NODE_ENV === 'development'
}
```
