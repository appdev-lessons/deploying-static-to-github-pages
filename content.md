# Deploying static web site to GitHub Pages

In the previous lesson you got your "Hello, World!" app running in the Codespace live application preview, published the changes to GitHub (commit and push), and got the tests to pass with `rake grade`.

Now it's time to actually deploy that static web site on the internet, so that anyone with the URL can visit it.

To do so, we will use GitHub Pages. 

## Enable GitHub Pages deployment

We've made a web page and we can see the results in our live app preview. But what if we want other people to be able to visit our site, and we want the site to be up and running even after we shut down our Codespace?

For that, we have to **deploy** our app to a hosting service. Fortunately, GitHub has yet _another_ great, free product for hosting static HTML websites, called GitHub Pages. Let's get that going!

Visit your repo's page (e.g. `github.com/<your-username>/hello-world`), click on "Settings", and then find "Pages" in the left sidebar. 

Under "Build and deployment", make sure the "Source" is set to "Deploy from a branch". Under the "Branch", use the dropdown menu to select `main` for the branch and `/(root)` for the location of your files, then click "Save":

<!-- ![](/assets/gh-pages-deploy-settings.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686166899/gh-pages-deploy-settings_jrye2b.png)
{: .bleed-full }

## Deploy!

Guess what? Your app is already online (or will be very soon)!

Because we enabled GitHub Pages deployment, anytime you push a commit to GitHub (which you should have done after you created the `index.html` file in your Codespace), your app will be built and deployed to GitHub's free hosting service.

<aside markdown="1">
At first, you may only find the content of the `README` file in the repo at `https://<your-username>.github.io/hello-world/`. If you don't have an `index.html` file in your repo in the `/(root)` folder, then GitHub Pages treats the `README` as that file and maps your homepage there.

And, how did the page actually deploy? If you visit the "Actions" tab in your code repository, you will see the "pages build and deployment" workflow that ran to deploy the static site. This GitHub Action will be run every time you make changes and publish them to the `main` branch of your repository!
</aside>

After you commit and push, return to your copy of the GitHub repository by navigating to `github.com/<your-username>/hello-world`. 

Visit the "Settings" > "Pages" tab in your `<your-username>/hello-world` repository. 

Refresh the page after a couple of minutes, and eventually you should see the note "Your site is live at `https://<your-username>.github.io/hello-world/`":

<!-- ![](/assets/gh-pages-settings-link-to-page.png) -->
![](https://res.cloudinary.com/dmxgp9oq2/image/upload/v1686167259/gh-pages-settings-link-to-page_ie0rd4.png)
{: .bleed-full }

If you visit the page by clicking "Visit site" to open in a new tab, you will see your deployed content: "Hello, world!".

You just built a website that anyone on the internet can visit 🎉

That domain `https://<your-username>.github.io` is provided to you for free by GitHub Pages, and any project repositories with static HTML and CSS that you deploy will be visitable at a URL path on that domain.

The `index.html` file has been mapped to the root of the `/hello-world` path. 

You can create as many GitHub Pages sites as you want! 
