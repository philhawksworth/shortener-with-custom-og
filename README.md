# URL Shortener with support for custom OG images

A URL shortener using [Netlify's](https://www.netlify.com/?utm_source=github&utm_medium=findthatat-pnh&utm_campaign=devrel) speedy CDN-based [Redirects API](https://www.netlify.com/docs/redirects/?utm_source=github&utm_medium=findthatat-pnh&utm_campaign=devrel)

Learn a little more about how this works [in the blog post](https://www.hawksworx.com/blog/find-that-at/)


## Show a custom OG image

Any short URLs you add which have a corresponding .png file in the `/dist/images` directory will unfurl in Twitter and other platforms to show this custom image instead of that included at the destination site.

Name images to match the short URL path thus:

`/dist/images/about.png` will be used as a custom OG image when sharing `https://example.com/about` 


## Try your own

You can use this repository to make your own url shortener with support for custom OG images.

1. Click the Deploy to Netlify button below (which clones this repo and uses your copy to create a new site on Netlify)
1. Follow the instructions to deploy your site
1. Create new short URLs by adding them to the `/_redirects` directory
1. Optional: Gve your new site a custom domain. (Good luck coming up with a snappy sounding short domain name :) )

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/philhawksworth/shortener-with-custom-og&utm_source=github&utm_medium=findthatat-pnh&utm_campaign=devrel)


## Local testing and development

After cloning the repo to your local dev machine, install the dependencies by running `npm i` from the project root directory.

Netlify Dev provides a local Edge Function environment and can make your local build accessible over the internet via a Netlify domain. A helper script does this for you. Run: `npm start`



## Adding a system wide `shorten` command 

This project uses [Kent C Dodds' utility for conveniently adding rules](https://github.com/kentcdodds/netlify-shortener#shell-function) to the `_redirects` file. He has provided [some helpful instructions on setting that up](https://github.com/kentcdodds/netlify-shortener#shell-function).

I also like to use [Raycast](https://raycast.com) to call that command for even easier creation of new URLs. ([Raycast command](https://gist.github.com/philhawksworth/b77d876e865ac190a6bb849913d4a744))
