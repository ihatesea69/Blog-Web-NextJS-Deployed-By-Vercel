# Blog-Web-NextJS-Deployed-By-Vercel

This repository contains a statically generated blog built using Next.js and Sanity. It includes a native Sanity Studio for content management, real-time collaboration, and visual editing. The blog is deployed via Vercel and is designed for a performant and customizable authoring experience.

## Project Overview

The project combines a Next.js frontend with Sanity for content management. Sanity provides a powerful Content Lake, enabling flexible query languages, image transformations, and more. The blog is fully editable with features like live content preview, real-time updates, and advanced custom field capabilities.

This project is ideal for those who want to set up a blog quickly with the ability to customize both the content structure and the visual experience.

### Features:
- Static blog with editable posts, authors, and site settings
- Native authoring environment (Sanity Studio) that is customizable
- Real-time collaboration and content editing with revision history
- Side-by-side preview that reflects changes across the site instantly
- Incremental Static Revalidation (ISR) for fast content updates
- Hosted Sanity project with unlimited admin users and free content updates
- TypeScript and Tailwind CSS for clean and modern development
- Free and easy deployment with Vercel

---

## Table of Contents

- [Project Overview](#project-overview)
- [Important files and folders](#important-files-and-folders)
- [Configuration](#configuration)
  - [Step 1: Set up the environment](#step-1-set-up-the-environment)
  - [Step 2: Set up the project locally](#step-2-set-up-the-project-locally)
  - [Step 3: Run Next.js locally in development mode](#step-3-run-nextjs-locally-in-development-mode)
  - [Step 4: Deploy to production](#step-4-deploy-to-production)
- [Questions and Answers](#questions-and-answers)
- [Next Steps](#next-steps)

---

## Important Files and Folders

| File(s)                             | Description                                                       |
|-------------------------------------|-------------------------------------------------------------------|
| `sanity.config.ts`                  | Config file for Sanity Studio                                     |
| `sanity.cli.ts`                     | Config file for Sanity CLI                                        |
| `/pages/studio/[[...index]].tsx`    | Mount point for Sanity Studio                                     |
| `/pages/api/revalidate.ts`          | Serverless route for triggering Incremental Static Revalidation   |
| `/pages/api/draft.ts`              | Serverless route for triggering Draft mode                       |
| `/schemas`                          | Defines content types for Sanity Studio                           |
| `/plugins`                          | Advanced customization for Sanity Studio                          |
| `/lib/sanity.api.ts`, `/lib/sanity.image.ts` | Configuration for Sanity Content Lake client                   |
| `/components/PreviewProvider.tsx`   | Configuration for live Preview Mode                               |

---

## Configuration

### Step 1: Set up the environment
1. Deploy the project using the "Deploy with Vercel" button to set up both the blog frontend and the Sanity Content Lake backend.

### Step 2: Set up the project locally
1. Clone the repository from your GitHub account.
2. Run the following command to link the project with Vercel:
   ```bash
   npx vercel link
   ```
3. Pull the necessary environment variables:
   ```bash
   npx vercel env pull
   ```

### Step 3: Run Next.js locally in development mode
1. Install dependencies and run the development server:
   ```bash
   npm install && npm run dev
   ```
2. The blog will be accessible at [http://localhost:3000](http://localhost:3000), and the Sanity Studio can be accessed at [http://localhost:3000/studio](http://localhost:3000/studio).

### Step 4: Deploy to production
1. To deploy changes to production, push your changes via Git:
   ```bash
   git add .
   git commit -m "Your commit message"
   git push
   ```
2. Alternatively, deploy via Vercel CLI:
   ```bash
   npx vercel --prod
   ```

---

## Questions and Answers

**It doesn't work! Where can I get help?**

- You can post your questions in the following communities:
  - GitHub Discussions for [Next.js](https://github.com/vercel/next.js/discussions)
  - [Sanity's GitHub Discussions](https://github.com/sanity-io/sanity/discussions)
  - [Sanity's Community Slack](https://slack.sanity.io/)

**How can I remove the "Next steps" block from my blog?**

- To remove the "Next steps" block, delete the `IntroTemplate` component located in `/components/IndexPage.tsx`.

**How can I set up Incremental Static Revalidation (ISR)?**

- Go to `/pages/api/revalidate.ts` for the code, where you’ll find instructions on setting up ISR.

---

## Next Steps

- Join the [Slack community](https://slack.sanity.io/) to ask questions and get further help.
- Learn how to customize your content structure and query your content.
- Explore [content modeling](https://www.sanity.io/docs/content-modeling) in Sanity.
