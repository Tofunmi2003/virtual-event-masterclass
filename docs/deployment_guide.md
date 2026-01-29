# 🚀 Deployment Guide: GitHub & Vercel

Since you haven't created a repository yet, follow these exact steps to get your Masterclass site live.

## Part 1: GitHub (Put your code in the cloud)
I have already initialized the **Git** repository on your computer and committed your files. Now we need to send them to GitHub.

1.  **Log in to GitHub** and go to [https://github.com/new](https://github.com/new).
2.  **Create a new repository**.
    *   **Repository Name**: `virtual-event-masterclass` (or whatever you like).
    *   **Public/Private**: Your choice.
    *   **Do NOT** check "Add a README", "Add .gitignore", or "Choose a license" (we already have these).
    *   Click **Create repository**.
3.  **Copy the commands** shown under the section **"…or push an existing repository from the command line"**.
    *   It will look like this:
        ```bash
        git remote add origin https://github.com/YOUR_USERNAME/virtual-event-masterclass.git
        git branch -M main
        git push -u origin main
        ```
4.  **Run those commands** in your terminal (VS Code).

---

## Part 2: Vercel (Make it live)
Once your code is on GitHub, Vercel makes deployment automatic.

1.  Go to [https://vercel.com](https://vercel.com) and Log In.
2.  Click **"Add New..."** -> **"Project"**.
3.  Select **"Continue with GitHub"**.
4.  You will see your new repository `virtual-event-masterclass`. Click **Import**.
5.  **Configure Project**:
    *   **Framework Preset**: Other (since we are using plain HTML/JS).
    *   **Root Directory**: `./` (Leave as default).
    *   **Build Command**: (Leave empty).
    *   **Output Directory**: (Leave empty).
6.  Click **Deploy**.

## 🎉 Done!
Vercel will give you a live URL (e.g., `virtual-event-masterclass.vercel.app`).
Every time you `git push` changes to GitHub, Vercel will automatically update your live site.
