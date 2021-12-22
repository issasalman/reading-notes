# React 3

## Assets


Next.js can serve static assets, like images, under the top-level public directory. Files inside public can be referenced from the root of the application similar to pages.

The public directory is also useful for robots.txt, Google Site Verification, and any other static assets. Check out the documentation for Static File Serving to learn more.

### Download Your Profile Picture
First, let's retrieve your profile picture.

* Download your profile picture in .jpg format (or use this file).
* Create an images directory inside of the public directory.
Save the picture as profile.jpg in the public/images directory.
* The image size can be around 400px by 400px.
* You may remove the unused SVG logo file directly under the public directory.

### Image Component and Image Optimization

Next.js also has support for Image Optimization by default. This allows for resizing, optimizing, and serving images in modern formats like WebP when the browser supports it. This avoids shipping large images to devices with a smaller viewport. It also allows Next.js to automatically adopt future image formats and serve them to browsers that support those formats.


### Using the Image Component
Instead of optimizing images at build time, Next.js optimizes images on-demand, as users request them. Unlike static site generators and static-only solutions, your build times aren't increased, whether shipping 10 images or 10 million images.

## Metadata
What if we wanted to modify the metadata of the page, such as the` <title>` HTML tag?
```
<title> is part of the <head> HTML tag, so let's dive into how we can modify the <head> tag in a Next.js page.
```
Open pages/index.js in your editor and find the following lines:
```
<Head>
  <title>Create Next App</title>
  <link rel="icon" href="/favicon.ico" />
</Head>
```
Notice that `<Head>` is used instead of the lowercase `<head>. <Head> `is a React Component that is built into Next.js. It allows you to modify the `<head>` of a page.

You can import the Head component from the next/head module.

Adding Head to first-post.js
We haven't added a `<title>` to our /posts/first-post route. Let's add one.

Open the pages/posts/first-post.js file and add an import for Head from next/head at the beginning of the file:

import Head from 'next/head'
Then, update the exported FirstPost component to include the Head component. For now, we‘ll add just the title tag:
```
export default function FirstPost() {
  return (
    <>
      <Head>
        <title>First Post</title>
      </Head>
      <h1>First Post</h1>
      <h2>
        <Link href="/">
          <a>Back to home</a>
        </Link>
      </h2>
    </>
  )
}
```
Try accessing http://localhost:3000/posts/first-post. The browser tab should now say “First Post”. By using your browser’s developer tools, you should see that the title tag is added to <head>.

To learn more about the Head component, check out the API reference for next/head.

If you want to customize the <html> tag, for example to add the lang attribute, you can do so by creating a pages/_document.js file. Learn more in the custom Document documentation.

## CSS Styling

As you can see, our index page (http://localhost:3000) already has some styles. If you take a look at pages/index.js, you should see code like this:
```
<style jsx>{`
  …
`}</style>
```
This page is using a library called styled-jsx. It’s a “CSS-in-JS” library — it lets you write CSS within a React component, and the CSS styles will be scoped (other components won’t be affected).

Next.js has built-in support for styled-jsx, but you can also use other popular CSS-in-JS libraries such as styled-components or emotion.

Writing and Importing CSS
Next.js has built-in support for CSS and Sass which allows you to import .css and .scss files.

Using popular CSS libraries like Tailwind CSS is also supported.


## What is React context?
React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.

In other words, React context allows us to share data (state) across our components more easily.

##  When should you use React context?
React context is great when you are passing data that can be used in any component in your application.


Why? Because context was not made as an entire state management system. It was made to make consuming data easier.

You can think of React context as the equivalent of global variables for our React components.

## What problems does React context solve?
React context helps us avoid the problem of props drilling.

Props drilling is a term to describe when you pass props down multiple levels to a nested component, through components that don't need it.

Here is an example of props drilling. In this application, we have access to theme data that we want to pass as a prop to all of our app's components.

As you can see, however, the direct children of App, such as Header, also have to pass the theme data down using props.