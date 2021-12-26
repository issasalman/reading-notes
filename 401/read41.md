# React 4
## Dynamic Routes
Dynamic routing refers to generating routes (URLs) to serve individual pages based on data which is subject to change.

Let's say we're making a blog using any old static site generator. The following data for our blog posts lives on a CMS which is queried by our static site generator at build time

## How does Next.js handle dynamic routing?
In Next.js, generating blog post pages based on JSON data is done by creating a page with a special filename, and implementing two functions: getStaticProps and getStaticPaths. These functions are the secret sauce behind how Next.js statically generates a bunch of pages.

I first tried to learn about them by reading Next.js' docs. I didn't really understand what I read, because I didn't have any live code samples to examine and tinker with.* I thought, maybe I can just make and break stuff until I see how these functions work together.

## Deploying Your Next.js App
### Push to GitHub

Before we deploy, let’s push our Next.js app to GitHub if you haven’t done so already. This will make deployment easier.

On your personal GitHub account, create a new repository called nextjs-blog.
The repository can be public or private. You do not need to initialize it with a README or other files.
If you need help setting up your repo, take a look at this guide on GitHub.
Then:

If you haven’t initialized the git repository locally for your Next.js app, do so now.
Push the Next.js app to your GitHub repository.
To push to GitHub, you can run the following commands (replace <username> with your GitHub username):

git remote add origin https://github.com/<username>/nextjs-blog.git
git push -u origin main


### Deploy to Vercel
The easiest way to deploy Next.js to production is to use the Vercel platform developed by the creators of Next.js.

Vercel is a serverless platform for static and hybrid applications built to integrate with your headless content, commerce, or database. We make it easy for frontend teams to develop, preview, and ship delightful user experiences, where performance is the default. You can start using it for free — no credit card required.

Create a Vercel Account
First, go to https://vercel.com/signup to create a Vercel account. Choose Continue with GitHub and go through the sign up process.

Import your nextjs-blog repository
Once you’re signed up, import your nextjs-blog repository on Vercel. You can do so from here: https://vercel.com/import/git.

You’ll need to Install Vercel for GitHub. You can give it access to All Repositories.
Once you’ve installed Vercel, import nextjs-blog.
You can use default values for the following settings — no need to change anything. Vercel automatically detects that you have a Next.js app and chooses optimal build settings for you.

* Project Name
* Root Directory
* Build Command
* Output Directory
* Development Command
* When you deploy, your Next.js app will start building. It * should finish in under a minute.

.

When it’s done, you’ll get deployment URLs. Click on one of the URLs and you should see the Next.js starter page live.


## Next.js and Vercel

* Vercel is made by the creators of Next.js and has first-class support for Next.js.
* When you deploy the following happens by default
1. pages that use Static Generation and assets will automatically be served from the Vercel Edge Network
2. pages that use Server-side Rendering and API routnes will automatically become isolated Serverless Functions.