# An Indie Guide to The IndieWeb
A simple guide to the IndieWeb by WIng Pang! Please let me know how I can improve this and feel free to add upon it as well.

This project was created based off [Max Boeck's eleventy-webmentions starter project](https://github.com/maxboeck/eleventy-webmentions).

It's been updated to the latest version of Eleventy and has support for:
- .webc web components (I used this quite a lot!)
- SASS/SCSS

## Installation

Installation: `npm i`
Dev: `npm run start`

## .webc Structure

I created reusable components for the whole project.

Each component has its own .scss stylesheet tied to it + is imported into components.scss.

I didn't use scoped .css since I wanted to use the features .scss has (like importing partials and mixins).

.scss components have `slot`s that you can insert elements into.

They're defined in the component via `name="namehere"` and can be used outside of it by using `slot="namehere"`.

Sometimes, you can get errors, but I figured out that it doesn't like it when you don't specify a class sometimes.

## To-do
[] Add webmentions

[] Add the fun shapes in the background

[] Consolidate any strange spacing

[] Add animations
