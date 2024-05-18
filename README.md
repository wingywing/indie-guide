# eleventy-webmentions

A basic starter template for [Eleventy](https://www.11ty.io) blogs with added support for [webmentions](https://indieweb.org/Webmention).  
For more information about this, read [Static Indieweb: Using Webmentions](https://mxb.at/blog/using-webmentions-on-static-sites/).

![Example of Webmention Section](https://mxb.at/assets/media/static-indieweb-webmentions/starter-template.png)

## Installation

Run `npm install` after cloning this repository. The available commands are identical to [eleventy-base-blog](https://github.com/11ty/eleventy-base-blog).

## Enable Webmentions

Follow these steps to get it working:

1. Go to [https://webmention.io/](https://webmention.io/) and sign in. To authenticate, you will have to include a `<a rel="me">` link at your domain, pointing to your github or twitter user URL:  

```<a href="https://github.com/maxboeck" rel="me">Max on Github</a>```

2. Once you've verified domain ownership, go to the [settings page](https://webmention.io/settings). Copy the token listed under "API Key" there.

3. Paste the token into the `.env.sample` file, then delete the `.sample` from the filename. That's a secret key, so this file should be in your `.gitignore`. If you are hosting your site on Netlify, make sure to [enter the token in your build settings](https://docs.netlify.com/configure-builds/environment-variables/#declare-variables).

4. Check the information in `_data/metadata.json` and make sure your domain name is correct.  It should look like `example.com`.

4. Run Eleventy. It will try to fetch the webmentions for your domain (you may not yet have any, check your webmentions.io [dashboard](https://webmention.io/dashboard)). After the first use, a cached json file will be created so you don't have to re-fetch that data everytime eleventy regenerates the site in development.

## Customization

This starter includes just the basic functionality, feel free to make it your own.  
The relevant parts are: 

* Templates: `_includes/webmentionlist.njk` and `_includes/webmention.njk`
* Filter: `webmentionsForUrl` in `.eleventy.js`
* Data Fetching: `_data/webmentions.js`
* Basic Styling: `css/webmentions.css`