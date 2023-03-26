# hosts

This will be a list of services that offers free web hosting.

## What I see recommended the most:

[**Github Pages**](https://pages.github.com/)

For free you get:

- 1 GB file size upload limit
- 1 GB storage space
- 100 GB bandwidth per month

Full limits: [About GitHub Pages - GitHub Docs](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages#usage-limits)

Github Pages is completely free forever. You can use it to host static websites with html, css, and javascript. You can write your own code, or you can use a [template.](https://pages.github.com/themes/) It works by serving files contained in a regular Github repository publicly on the web. Your site will be available on a .github.io subdomain. You can use custom domains with Github Pages, but you need to obtain the domain from a domain name provider, which is almost never free.

[**Gitlab Pages**](https://docs.gitlab.com/ee/user/project/pages/)

For free you get:

- 5 GB storage space
- 10 GB transfer per month
- 400 compute minutes per month
- 5 users per name space

Full limits: [Pricing | GitLab](https://about.gitlab.com/pricing/)

Gitlab Pages is completely free forever. It works just like Github Pages: it supports static sites in html, css, and javascript and serves files contained in Gitlab repos. You can write your own code or use a [template.](https://gitlab.com/pages) Sites are available on a .gitlab.io subdomain. You can use custom domains.

[**Codeberg Pages**](https://codeberg.page/)

Codeberg Pages is completely free forever. It works just like the other two git services above: it supports static sites in html, css, and javascript and serves files contained in Codeberg repos. You can write your own code or use a template. Sites are available on a .codeberg.page subdomain. You can use custom domains.

As far as I know, as far as I can find, Codeberg has **no** bandwidth or storage limits. But I wouldn't recommend them if you have a very high-traffic site because Codeberg is a completely free and open-source platform that only makes money from user donations, and I don't know what their servers can handle. Basically, just don't be selfish.

[**Netlify**](https://www.netlify.com/)

For free you get:

- 1 concurrent build
- 100 GB bandwidth per month
- unlimited storage space (but larger sites lose performance)

Full limits: [Netlify Pricing and Plans](https://www.netlify.com/pricing/)

Netlify is free forever, but it does charge you if you go over the limits of your chosen monthly plan. In this case for example, on the free plan if you go over 100 GB bandwidth in a month, they charge you for the data that goes over it.

...

**Of these four services,** I have only personally used Github Pages. I have never had any problems with Github Pages and I used it for about 4 years in a row uninterrupted. I see Netlify recommended to people on Reddit a lot, but I would not consider using it if you're in a situation where you absolutely can't afford to pay for anything. It's really unlikely that you could go over their 100 GB bandwidth per month limit, or any of their other limits, but why risk it?

***Luckily, there are still many more options for free hosting providers.***

...

## Other services I often see recommended:

[**Neocities**](https://neocities.org/)

For free you get:

- 1 GB storage space
- 200 GB bandwidth per month

Full limits: [Neocities - Become a Supporter](https://neocities.org/supporter)

Neocities is open source and completely free forever, or as long as the service runs. Sites hosted by Neocities are available on a .neocities.org subdomain. You can use a custom domain, but only if you pay for a premium account. You can edit your site directly in their online code editor or you can upload files from your computer. Neocities also offers a [free course]([Neocities - HTML Tutorial - 1/10](https://neocities.org/tutorial/html/1)) on how to code basic html and css. Basic html and css is very easy to learn, so don't feel intimidated!

[**Surge**](https://surge.sh/)

For free you get:

- unlimited bandwidth

- basic SSL

Full limits: [Pricing • Surge](https://surge.sh/pricing)

Surge is free to use forever, however free accounts are heavily limited compared to paid accounts. Still, unlimited bandwidth for free isn't very common! Surge runs on your local machine and publishes whatever directory you run it in to the web. Free sites hosted by surge are available on a .surge.sh subdomain. You can use a custom domain with Surge, but they don't register domains so you'll have to obtain your custom domain from a dedicated domain name provider.

## Other services I've heard of:

These are other services I've heard of, I've used some of them, and I've researched them all fairly well.

[**Cloudflare Pages**](https://pages.cloudflare.com/)

For free you get:

- 1 build at a time

- 500 builds per month

- unlimited bandwidth

Full limits: [Cloudflare Pages Pricing](https://pages.cloudflare.com/#pricing)

With Cloudflare Pages you can either edit your sites code locally on your computer with your preferred editor and then upload the files to Cloudflare, or connect your Cloudflare account with your Github account and deploy to Cloudflare from a Github repository. Free sites are available on a .pages.dev subdomain. You can use a custom domain, but you have to pay for them.

Cloudflare is a very trusted name online, its CDN is used by a staggering amount of the web: some estimates show that more than 20% of known websites on the internet are using Cloudflare services in some way. The reason it's not mentioned until this late in this article is simply that I've never seen *anyone* recommend Cloudflare Pages to host personal static websites. Because it is such a stable and trusted CDN, I personally currently serve media files for my own personal website with Cloudflare.

[**render**](https://render.com/)

For free you get:

- 400 build hours per month

- 100 GB bandwidth per month

Full limits: [Static Sites | Render · Cloud Hosting for Developers](https://render.com/docs/static-sites)

render works similarly to Cloudflare Pages: you can connect to Github or Gitlab and deploy your site from a repository. Free sites are available on a .onrender.com subdomain. You can use custom domains with render, but you'll have to obtain one from a dedicated domain name provider. Like Netlify, render will charge you if you go over their limits, so if you *absolutley cannot* put any money toward your website, render may not be the best choice to start with.

[**Amazon Web Services**](https://aws.amazon.com/)

For free you get:

- 15 GB storage

- 15 GB bandwidth per month

Full limits: [AWS Product and Service Pricing | Amazon Web Services](https://aws.amazon.com/pricing/?nc2=h_ql_pr_ln&aws-products-pricing.sort-by=item.additionalFields.productNameLowercase&aws-products-pricing.sort-order=asc&awsf.Free%20Tier%20Type=free-tier%23always-free&awsf.tech-category=*all)

Amazon Web Services is another very trusted platform for web hosting. Some of the companies that rely on AWS to host and serve their products include Facebook, Twitter, Netflix, Hulu, and Twitch. While they do serve less of the web than Cloudflare, they do serve many of the most popular websites on the web. That being said, AWS is another pay-as-you-go service, very much like Netlify and render. This means that if you exceed the limits on free accounts, you'll get charged. So, again, if you *absolutely cannot* put any money toward your website, AWS may not be the best choice to start with.

[**ichi city**](https://ichi.city/)

ichi city is open source and completely free forever. I have no idea what the hosting limits are. ichi city seems to be a personal project of [m15o](https://m15o.ichi.city/) and I'm not really sure how the project is funded, so I imagine it would be ideal to not upload very large sites or high traffic sites here. ichi is also explicitly not for advertising, so if your website is just self-promotion you shouldn't use ichi city.

[**tilde town**](http://tilde.town/)

tilde town is also open source and completely free forever. I don't know what the hosting limits are, and tilde appears to be funded entirely by user donations.

## Even more services I've heard of:

Please use any of the following hosting providers at your own risk. I've not only never used any of these, I've barely done any research into them. I've seen some of them recommended here and there, I've seen some of them almost never recommended, I've seen some of them get very negative reviews, and I discovered many of them by stumbling on them through search results instead of through recommendations. I've heard rumors that some of these hosts delete websites without warning for even slightly going over bandwidth, processing, or storage limits. Please only use any of the following hosts if you do your own independent research into them or if you, for some reason, are unable to use any of the ones I mentioned in the earlier sections.
