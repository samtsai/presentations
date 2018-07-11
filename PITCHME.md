# Front-End Primer

---

# Overview

@ul

- Single Page Applications (SPAs)
- Progress Web Apps (PWAs)
- Native App Development

@ulend

---

# Single Page Applications (SPAs)

---

### Often understood as:

- "snappy" - does not fully reload when navigating around / just data sent over the wire
- version-able and easily deployed (push up new static files and update `index.html`)
- associated with a popular framework (Ember, Angular, React, etc)

---

## One "Page" (`index.html`)

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="utf-8">
    <meta http-equiv="cache-control" content="no-cache, must-revalidate, post-check=0, pre-check=0">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta http-equiv="expires" content="0">
    <meta http-equiv="pragma" content="no-cache">
    <title translate="Page Title">Client Portal</title>
    <base href="/">
    <meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=0" />
    <link rel="icon" type="image/x-icon" href="favicon.ico">
    <script language="javascript" async="true" type="text/javascript" src="//whatfix.com/0ba0dac0-162d-11e7-b2bb-04013d24cd02/embed/embed.nocache.js"></script>
    <link href="styles.74cac7c9e4341196f1e3.bundle.css" rel="stylesheet" />
</head>

<body>
    <app-root></app-root>
    <script type="text/javascript" src="inline.65c5fb0271f41fdaf0a8.bundle.js"></script>
    <script type="text/javascript" src="polyfills.2e9e8afa0200310444f7.bundle.js"></script>
    <script type="text/javascript" src="main.6951675455407aea22cf.bundle.js"></script>
</body>

</html>
```

- CSS bundle, JS bundle, Angular container

Notes:
Implicitly this means templating (or rendering) of data from some API(s) is built into the application framework.

---

## SPA Hate Mail

- Search engine ranking (aka SEO) / Inaccessible
- Going to fail / Unsaved changes / Memory leaks
- (mine): Business logic duplication
- History and fast back / Scroll position / Cancelling navigation
- Loading CSS and JS / Probably slower / Loading indicators
- Analytics / Automated functional testing

---

> Javascript is never going to beat the browser at what it does best—browsing. We can still give users rich and enhanced experiences without cramming an entire site into one document.
> We should let the browser manage the browsing experience, and spend our time solving real problems.[^2]

See also: https://medium.freecodecamp.org/why-i-hate-your-single-page-app-f08bb4ff9134

[^2]: [The disadvantages of single page applications](https://adamsilver.io/articles/the-disadvantages-of-single-page-applications/) - Adam Silver

---

## TL;DR

My interpretation:

> With SPAs you're no longer building for the platform (web browser)
but forced into writing logic to mimic the platform as closely as possible.
Which takes away from the main goal of writing code to solve real problems.

---

# Alternatives

Server Side w/ Dynamic Pages:

- ASP.NET Core with [Razor Pages](https://docs.microsoft.com/en-us/aspnet/core/tutorials/razor-pages/razor-pages-start?view=aspnetcore-2.1)
- [Blazor](https://blazor.net/) but not anytime soon

---

# Resources

- [Wikipedia: SPA](https://en.wikipedia.org/wiki/Single-page_application)

# Progressive Web Apps (PWAs)

---

Compared to Native Apps

- high friction download to install app
- deep linking often lost

---

Limitations

Not all browsers support PWAs and have varying degree of support

---

## Resources

### Angular

https://houssein.me/progressive-angular-applications

### Metrics

- https://www.pwastats.com/

### Examples

- [Financial Times](https://app.ft.com/index_page/home)
- Flipkart
- [Twitter Lite](https://lite.twitter.com/content/lite-twitter/en.html)
- [HNPWA](https://hnpwa.com/)

### Case Studies

- https://medium.com/dev-channel/treebo-a-react-and-preact-progressive-web-app-performance-case-study-5e4f450d5299
- https://blog.twitter.com/engineering/en_us/topics/open-source/2017/how-we-built-twitter-lite.html
- https://medium.com/elemefe/upgrading-ele-me-to-progressive-web-app-2a446832e509
- https://medium.com/dev-channel/a-pinterest-progressive-web-app-performance-case-study-3bd6ed2e6154