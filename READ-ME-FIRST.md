# Putting the Inclusive Hiring Companion online

This folder is a complete site. It has three things:
- index.html (the companion people see)
- api/chat.js (the small backend that holds your secret key)
- package.json (a required config file, you do not edit it)

You will deploy it to Vercel, the same place Values Align lives. Here is the whole process.

## What you need first
Your Anthropic API key. It starts with sk-ant- and you get it from console.anthropic.com under API Keys. Keep it private. It never goes in the HTML; it only goes into Vercel as a setting.

## Option A: drag and drop (simplest)
1. Go to vercel.com and sign in.
2. Click Add New, then Project.
3. Drag this whole folder onto the upload area.
4. Before you click Deploy, open the Environment Variables section.
5. Add one variable:
   - Name: ANTHROPIC_API_KEY
   - Value: your sk-ant- key
6. Click Deploy. In about a minute you get a public link like inclusive-hiring.vercel.app.

## Option B: through GitHub (matches your Values Align setup)
1. Put this folder in a new GitHub repo (for example, karabedleadershipgroup/inclusive-hiring).
2. In Vercel, Add New, Project, and import that repo.
3. In Settings, Environment Variables, add ANTHROPIC_API_KEY with your key.
4. Deploy. After this, every time you push changes to GitHub, Vercel updates the site automatically, just like Values Align.

## How to test it worked
Open the link, pick Ask for Guidance, type a sentence, and send. If you get a real response, the backend and key are wired correctly. If you see "Something went wrong," the key is missing or misspelled in Vercel.

## Good to know
- The Curriculum Refresher slides work no matter what, since they are static.
- The four chat modes only work once the key is set in Vercel.
- Anyone with the link can use it, and every message uses your API key, so each conversation costs a small amount against your Anthropic account. If you want to limit who can use it, tell me and I can add a simple access code gate later.
