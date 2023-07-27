# tutorial install tailwindcss with Next.js
https://www.youtube.com/watch?v=kap8xrWMNDM

npx create-next-app example with-tailwindcss

# tutorial learn Next
https://www.youtube.com/watch?v=NgayZAuTgwM

# install dependency for API //explanation min 2 - 6.
npm i prisma --save-dev
npx prisma init --datasource-provider sqlite
add a model to schema.prisma
* Explanation tutorial video from min 2 to 3:30 m
npx prisma migrate dev --name init

# start the app
npm run dev

# Steps
1. Get the correct configuration of tailwind.confif.js:
* When I tried before tailwind wasnt working coz I' need to make some change in tailwind.config.js. I need to put the correct root for app. It come by default like this:
    './app/**/*.{js,ts,jsx,tsx,mdx}',
Since I created the folder src and put app inside this folder, the correct root is:

    './src/app/**/*.{js,ts,jsx,tsx,mdx}',

2. Get some global CSS setting in globals
* This is by default:

        className={inter.className}
      >
        {children}
* This is how the tutorial shows it. It will have a dark background, light letter and responsive:

        className={`${inter.className} bg-slate-800 text-slate-100 container mx-auto p-4`}
      >
        {children}

3. Create routes:
Create a new folder inside app folder. Inside this this folder, create a file name <page.tsx>
3.1 Inside app, <page.tsx>:
<Link href="/new">New</Link>

4. components/TodoItem.tsx
It containts a check box. the dinamy style is not working

className="cursor-pointer peer-checked:line-through peer-checked:text-slate-500"
* explanation min 18. I did exactly still does not work

5. new/page.tsx
form working with console.log
