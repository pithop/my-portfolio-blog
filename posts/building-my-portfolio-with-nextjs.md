---
title: "Building My Portfolio with Next.js"
date: "2025-06-12"
excerpt: "Introduction

As a web developer, showcasing my skills through a personal portfolio is essential. I "
---

Introduction

As a web developer, showcasing my skills through a personal portfolio is essential. I chose Next.js for its powerful features like server-side rendering and static site generation. This post details how I built my portfolio website, the challenges I faced, and the solutions I implemented.

Why Next.js?

Next.js offers a robust framework for building fast, SEO-friendly websites. Its App Router simplifies dynamic routing, and Vercel makes deployment seamless. I used Tailwind CSS for styling and integrated the GitHub API to manage blog posts dynamically.

Key Features

Dynamic Blog: Posts are fetched from a GitHub repository, allowing easy content updates without redeploying.

Password-Protected Submission: A custom API route secures blog post submissions with a daily password.

Responsive Design: Tailwind CSS ensures the site looks great on all devices.

Challenges and Solutions

One challenge was handling fetch errors when integrating the GitHub API. Initially, I encountered a "TypeError: fetch failed" error due to a missing GITHUB_TOKEN. I resolved this by adding error handling and ensuring environment variables were set in Vercel.

Code Example

Here’s how I fetch blog posts from GitHub:

const response = await fetch(`https://api.github.com/repos/pithop/my-portfolio-blog/contents/posts`, {
  headers: {
    Authorization: `token ${process.env.GITHUB_TOKEN}`,
  },
});
const files = await response.json();

Lessons Learned

Error Handling: Always wrap API calls in try-catch blocks to prevent crashes.

Environment Variables: Double-check variables in production to avoid undefined errors.

Documentation: Next.js and GitHub API docs were invaluable for troubleshooting.

Conclusion

Building my portfolio with Next.js was a rewarding experience that deepened my understanding of modern web development. I encourage other developers to experiment with Next.js for their projects. What’s your favorite framework? Share in the comments
