
## Getting Started
http://social-media-twitter-clone-qwnc71f7c-jins-projects-a7432597.vercel.app

This project was deployed on Vercel, for visiting the website, click the url link above.

This project is a Twiiter-liked social media clone as a personal project. By using it, you can create an account, edit your personal profile, upload your cover image and profile image, post messages, follow somebody and like other posts.



For making this project:

React is used for the frontend, NextJS is used for routing and server sied rendering, Tailwind for css management, Prisma is used for database management, and MongoDB for backend storage.




## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## Problems I faced during the Deployment process

https://www.prisma.io/docs/orm/more/help-and-troubleshooting/help-articles/vercel-caching-issue

If you are working on a project which also using Prisma for database management, during the deployment process on Vercel, you may face an error like this:

```bash
Prisma has detected that this project was built on Vercel, which caches dependencies.
This leads to an outdated Prisma Client because Prisma's auto-generation isn't triggered.
To fix this, make sure to run the `prisma generate` command during the build process.

Learn how: https://pris.ly/d/vercel-build
```

This is mainly because Vercel caches the dependencies of projects until one of those dependencies changes. And you can easily solve this error in two ways by following the docs, the url link above.
