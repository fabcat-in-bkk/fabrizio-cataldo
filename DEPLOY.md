# How to put this website on the internet

You need two things: a Vercel account (free) and about five minutes.

---

## Step 1. Unpack the folder

Download `fabriziocataldo-site.tar.gz` and double click it. You get a folder.
Rename that folder to `fabriziocataldo` and move it somewhere you will find again,
for example your Desktop.

Inside you should see:

    index.html      the website
    cv/index.html   the CV page
    og.png          the preview image for links
    robots.txt
    sitemap.xml
    vercel.json

---

## Step 2. Install the Vercel command line tool

Open Terminal (press Cmd+Space, type "Terminal", press Enter) and paste this:

    npm install -g vercel

Press Enter. Wait for it to finish.

If it says "npm: command not found", install Node.js first from https://nodejs.org
(download the LTS version, run the installer, then close Terminal, open it again,
and run the command above).

---

## Step 3. Go into the folder

In Terminal, type `cd ` (with a space after it), then drag the `fabriziocataldo`
folder from your Desktop into the Terminal window. It fills in the path for you.
Press Enter.

To check you are in the right place, type `ls` and press Enter. You should see
`index.html` in the list.

---

## Step 4. Deploy

Type this and press Enter:

    vercel --prod

The first time, it asks you a few questions. Answer them like this:

| Question | Answer |
|---|---|
| Set up and deploy? | press Enter for yes |
| Which scope? | press Enter for your personal account |
| Link to existing project? | type `n`, press Enter |
| What's your project's name? | type `fabriziocataldo`, press Enter |
| In which directory is your code? | press Enter to accept `./` |
| Want to modify these settings? | type `n`, press Enter |

If it asks you to log in first, it opens your browser. Sign in with GitHub, Google
or email, then come back to Terminal.

After about twenty seconds it prints a line like:

    Production: https://fabriziocataldo.vercel.app

Open that link. That is your website, live.

---

## Step 5. Check it works

Open the link on your phone as well as your laptop. Check:

- the site loads and scrolls
- "Read the CV" opens the CV
- add `/cv` to the end of the URL and it loads as its own page
- "Book a call" opens your calendar
- the email button opens a new email

---

## Step 6. Buy the domain

In your browser go to https://vercel.com/dashboard and click the
`fabriziocataldo` project.

1. Click **Settings** in the top menu
2. Click **Domains** in the left sidebar
3. Type `fabriziocataldo.com` in the box and click **Search** or **Buy**
4. Pay. It is about $11.25 a year
5. Vercel connects it automatically

Wait a few minutes, then open https://fabriziocataldo.com

---

## Making changes later

Edit the files, then in Terminal go to the folder again and run `vercel --prod`.
It replaces the live version. There is no build step, so it is always this fast.

If you break something, go to the project in the Vercel dashboard, click
**Deployments**, find an older one, click the three dots and choose
**Promote to Production**. That puts the old version back immediately.
