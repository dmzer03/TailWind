# Demo miniproject to Practise Tailwind CSS

#  TailWind Notes as well here 
Tailwind:
-----------------------------------------------------------
"Rapidly build modern websites without ever leaving your HTML."

"Utility-first" means the framework's main focus is on providing utility classes.

Advantage:
Eliminates the Confusion.
Production final bundle size is less.
----------------------------------------------------------------
=> 2 Popular way to use tailwind :
1.CDN : Good for development but not for productions.
In Console: 
(index):61 cdn.tailwindcss.com should not be used in production. To use Tailwind CSS in production, install it as a PostCSS plugin or use the Tailwind CLI: https://tailwindcss.com/docs/installation

<script src="https://cdn.tailwindcss.com"></script> Just add this tags.


2.Using Tailwind CLI:Node.js should installed for this method.
By Using PostCSS
-> : npm install -D tailwindcss postcss autoprefixer
-> : npm i vite 
-> : npx tailwindcss init -p : Will create postCSS.config file

/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["*"], //* or individual file name.
  theme: {
    extend: {},
  },
  plugins: [],
}

-> Create one CSS file with any name. Add the below 3 Snippets.
 @tailwind base;
 @tailwind components;
 @tailwind utilities;

-> Add below thing to package.json 
 "scripts": {
    "start": "vite"
  }

-> link css sheet to HTML 

-> Start your server 
-> npm run start
-----------------------------------------------------------
Typography & Sizing :
Scaling : 1 = 0.25rem
          4 = 1 rem = 16px 
          ml-4 ( 1 rem from left ) 
          m-4  ( 1 rem from all directions)
          mx-4 ( 1 rem from left & right means horizontal)
          my-4 ( 1 rem from top  & bottom means vertically)


text-color.
background-color.

Spacing : 
Margin: ml- ,mr- ,mt- ,mb- 
Padding: =//= ,=//=,=//= (same as above)
Space : Space between the child elements.
<-flex space-y*-4 -> applied on only from 2nd and 3rd not on first 

h-[200px]:Square brackets notations : to give in pixel values.
Will be consider as valid.But dont used frequently.It creates a new class and style increases the bundle size.

For responsive Design:
BreakPoints:
Ex: md:w-32 lg:w-48
    sm:bg-green-500 md:bg-purple-700

Apply Directive: 
use @apply to inline any existing utility classes inot your own custom css.
generally any styling repeats then we can use this.

always given the priority to last written code in css file.

Background image : Gradient is below present.
