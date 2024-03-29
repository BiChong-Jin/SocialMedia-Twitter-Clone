
## About This Project

http://social-media-twitter-clone-qwnc71f7c-jins-projects-a7432597.vercel.app

This project was deployed on Vercel, for visiting the website, click the url link above.

This project is a Twiiter-liked social media clone as a personal project. By using it, you can create an account, edit your personal profile, upload your cover image and profile image, post messages, follow somebody and like other posts.



For making this project:

- React for the frontend
- NextJS for routing and server side rendering
- Tailwind for css management
- Prisma for database management
- MongoDB for backend storage


## Learn More About Next.js

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

## Possible errors you may face during the connecting process of MongoDB Atlas

- The connection string
  
For the varation of the version of MongoDB Atlas, the provided form of connection string may not be the correct form for you. In this project, connection string for VS code have been used. The connection string provided by MongoDB Atlas was something like this:

```bash
mongodb+srv://<Your Account Name>:<Your Password>@<Your Database Name>.<Random string>.mongodb.net/
```

However, if you just use this form of the string, I think you probably will face a error when you do ``` prisma db push ```. To solve this problem, you need arrange the string's form a little bit :

```bash
mongodb+srv://<Your Account Name>:<Your Password>@<Your Database Name>.<Random string>.mongodb.net/<Your Collection Name>?retryWrites=true&w=majority
```

So basically you should add the context above after " net/ ", and for the collection name part, you can just name whatever you want. And in fact, if you have a look of the doc, this part will auto generate for you.

- The access IP address

When you successfully connected to you Mongo firstly, after a period, you may lose the connection of it. It may caused by multi factors, but one of the most common possible problem is the setting of the access IP address in you Mongo. If you are in a Wi-Fi environment, your IP address might be a " Dynamic IP address ", and its means that it will auto-change when you restart your PC or reconnect your Wi-Fi. And in Mongo, they have a control of the accessing of the IP address. For letting all IP address be able to connect to your database, you can go to your " Network Access " section. and click " Add IP Address ". And put ``` 0.0.0.0/0``` in it, it will allow all IP address to connect to your db. 
 
