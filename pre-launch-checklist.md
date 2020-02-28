# Pre Launch Checklist

This is a simple checklist that should be ran over completed builds, please note that this is a top level overview on basic website standards that all builds should aim to adhere to (no excuses!). Thorough business logic checks should be created bespoke on a per project basis, e.g checkouts, booking systems, custom made CMS's etc.

## Head

- [ ] The Doctype is HTML5 at the top of all the pages on the site `<!doctype html`
- [ ] The website charset is declared correctly (UTF-8) `<meta charset="utf-8">`
- [ ] The viewport is set correctly `<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">`
- [ ] A title is set for every page of the website.
- [ ] A meta description is set for every page of the website.
- [ ] No meta keyword tags are used at all across the website.
- [ ] Favicons / Apple Touch icons have been created and display correctly across browsers.
- [ ] Canonical links have been set in the header to avoid any duplicate content across the site. `rel="canonical"`
- [ ] Language attribute has been set, ensuring the attribute correctly matches the language in use on the page. For Bilingual websites ensuring this tag updates as the language changes.
- [ ] Conditional comments are set for IE such as the HTML5 shiv etc.
- [ ] Inline critical CSS is minified and injected into the head.
- [ ] CSS files are loaded before any JavaScript within the HEAD.

## HTML

- [ ] Semantic HTML5 elements are in use across the website `<main> <section> <aside>` etc

- [ ] An error 404 page has been setup on the website and functioning as intended, ensuring the information on the page is actually useful to the user.

- [ ] All external links using `target="_blank"` are supported with a `rel="noopener"` attribute to reinforce security and prevent 'tab nabbing'.

- [ ] Unnecessary comments have been removed from all pages across the website.

- [ ] All pages adhere to W3C compliancy rules, though take some of this with a pinch of salt!

- [ ] There are no broken links anywhere on the website.

  https://www.screamingfrog.co.uk/ site crawler should aid in this.

- [ ] No Lorem Ipsum text, or placeholder text is present on the website, and any test pages should be removed.

## Web Fonts / Icons

- [ ] All web fonts are loading and rendering correctly across all browser and platforms. Keep close eye out for line height variation and dodgy characters.
- [ ] Web font file sizes are kept to a minimum, keeping below 2mb is advised here.
- [ ] If using a third party font provider such as Typekit, ensure this has been transferred over to the clients own details before launch.
- [ ] Icons on the site are rendered in the form of SVGs, whilst avoiding the use of Icon Fonts unless specified otherwise or requested by the client. This is to ensure we maintain a high standard for accessibility.

## CSS/SCSS

- [ ] All SCSS/CSS has it's properties listed out in alphabetical order.
- [ ] All classes are being specified in a BEM (block element modifier) structure, unless the project standards requests otherwise.
- [ ] Nesting in SCSS is kept to a minimum, ensuring we're going no more than 2 deep. This aids maintainability.
- [ ] REM/EM units are used throughout to ensure the browser remains scalable if the user increases / decreases their browsers default font size. Exceptions lie for things like borders where you're specifying 1px widths.
- [ ] JS prefixed classes are not being styled with, these classes are for use with JS ONLY.
- [ ] No CSS is inline in a `<style>` tag with the exceptional of critical baseline CSS styles.
- [ ] All CSS is being correctly minified when put live for production.
- [ ] All browser prefixes are being correctly added in to maintain browser compatibility.

## Browser / OS Testing

A full test for the browsers below have been performed

- [ ] Internet Explorer 11+
- [ ] Edge
- [ ] Chrome (Additional Chromium based browsers such as Brave, Opera would be a bonus too)
- [ ] Firefox
- [ ] Safari

A full test of the various OS types below have been performed:

- [ ] Windows
- [ ] MacOS
- [ ] iOS
- [ ] Android

## Forms / Emails

- [ ] All forms on the website have been tested, whether through mailtrap.io or test emails.
- [ ] Form Validation is in place where necessary, with descriptive information being provided to help the user.
- [ ] Success / Fail messages have been setup correctly, giving the user a clear indication when something has been submitted.
- [ ] Email templates have been tested through any means possible, and are working nicely across a variety of mail clients.

## JavaScript

- [ ] JavaScript is following a component based structure.
- [ ] All JavaScript is being wrote in ECMAscript 6 (ES6) first and foremost, to ensure futureproofing and cleaner more concise code.
- [ ] All ES6 code is being correctly transpiled via Babel into readable code for older browsers.
- [ ] All JS is written in camelcase.
- [ ] Any polyfills added into the project have been tested and confirmed to be working correctly.
- [ ] All NPM packages in use are fully up to date prior to launch.
- [ ] No console errors are appearing on the site.
- [ ] Unneeded comments and `console.log()` have been removed from the JS.
- [ ] If building for WordPress, jQuery has been deactivated from the theme.
- [ ] Any unwanted components left over from the boilerplate has been removed.
- [ ] All JS has been minified ready from production.

## Imagery

- [ ] All images have been optimised and compressed to a good standard.
- [ ] Picture/srcset has been used where possible to provide the most appropriate image for the current viewport.
- [ ] Alt text has been added to all the imagery, making sure it's all descriptive and relevant to what the image actually is.
- [ ] Lazyloading has been utilized across the website, preferably with a preloader effect.

## Accessibility

- [ ] Colour contrast should be reasonable, making sure text and important details on the site are comfortably readable / understandable.

- [ ] Critical site functionality like main menus should all be operable without JavaScript.

- [ ] The site should be comfortable to get around via a keyboard.

- [ ] If focus is disabled, then this should be replaced by visible state in CSS.

- [ ] `aria-label` attributes are being correctly and liberally used across the website to aid accessibility. e.g for use cases like below:

  `<button aria-label="Close" type="button">X</button>`

  e.g The above will help screen reader users understand what the button is doing, to a user with full vision we can see it's a close button, but to a screen reader user it's less obvious.

- [ ] A cross section of the site has been tested via WAVE webaim accessibility test, ensuring all errors have been resolved where possible: https://wave.webaim.org/

## Performance

- [ ] Page weight should be kept to a minimum, any pages over 1mb should be investigated to ensure everything has been done to keep size to a miniumum.

- [ ] HTML has been minified.

- [ ] Lazy loading has been implemented for images, scripts and css, this will increase the response time of the page.

- [ ] Third party libraries and components have been vetted, components using excessive external API calls should be investigated.

- [ ] All image assets have been minified using an image compressor such as ImageOptim (Mac), FileOptimizer (Windows).

- [ ] Website has been ran through Google Pagespeed Insights, and any critical errors have been resolved:

  https://developers.google.com/speed/pagespeed/insights/

## SEO

- [ ] Google Analytics has been added to the site using the clients own details. This has also been fully tested in the live overview to be working.
- [ ] A sitemap.xml file has been created for the website, and submitted to the clients Google Search console if required.
- [ ] A baseline robots.txt has been constructed for the website, ensuring no pages are being blocked that shouldn't be.
- [ ] A HTML sitemap has been created, with a full list of links for the websites main pages.
- [ ] Heading hierarchy has been correctly structured on the page, this helps crawlers understand how the page fits together.

## Documentation

- [ ] Any complex functionality on the site has been well documented so other developers can pick the project up and understand what's going on.
- [ ] The project README.md has the full technology stack listed out e.g PHP 7 / Laravel / Laravel Mix / JavaScript ES6+ / React.js / SCSS
- [ ] The project README.md has all the node packages in use listed out, accompanied by a link to the packages documentation / github repo.

## GIT Process

- [ ] Prior to launch the MASTER branch has been updated to the latest production version.
- [ ] Any unneeded branches have been closed.
- [ ] the .gitignore file is up to date and no unwanted files are being included in the repo, such as .env files or compiled assets. Any sensitive information has also been removed, such as any stored database, password information.
