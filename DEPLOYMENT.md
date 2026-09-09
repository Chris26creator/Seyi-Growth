# Deployment Guide - Seyi Growth

Complete instructions for pushing your code to GitHub and deploying your website.

## 📤 Step 1: Push to GitHub

### Option A: Using GitHub CLI (Easiest)

If you have GitHub CLI installed:

```bash
cd /path/to/seyi-growth
git remote add origin https://github.com/Chris26creators/seyi-growth.git
git branch -M main
git push -u origin main
```

### Option B: Using Git with HTTPS

1. **Create a Personal Access Token** on GitHub:
   - Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Click "Generate new token"
   - Select scopes: `repo`, `workflow`
   - Copy the token

2. **Push your code**:
```bash
cd /path/to/seyi-growth
git remote add origin https://github.com/Chris26creators/seyi-growth.git
git branch -M main
git push -u origin main
```

When prompted for password, paste your Personal Access Token.

### Option C: Using SSH (If configured)

```bash
cd /path/to/seyi-growth
git remote add origin git@github.com:Chris26creators/seyi-growth.git
git branch -M main
git push -u origin main
```

---

## 🚀 Step 2: Deploy to Vercel (Recommended)

### Automatic Deployment (Easiest)

1. Go to [vercel.com](https://vercel.com)
2. Click **"Add New"** → **"Project"**
3. Select **"Import Git Repository"**
4. Search for and select `seyi-growth`
5. Click **"Import"**
6. Vercel will auto-detect Next.js
7. Click **"Deploy"**

**That's it! Your site is live.** Vercel will automatically:
- Build your project
- Deploy to production
- Set up automatic deployments on every push

### Add Custom Domain

In Vercel Dashboard:
1. Go to your project
2. Settings → Domains
3. Add your domain
4. Update DNS settings (Vercel will provide instructions)

---

## 🌐 Step 3: Deploy to Netlify (Alternative)

### Option 1: Via Netlify UI

1. Go to [netlify.com](https://netlify.com)
2. Click **"Add new site"** → **"Import an existing project"**
3. Choose GitHub
4. Authorize and select `seyi-growth`
5. Leave build settings as default
6. Click **"Deploy"**

### Option 2: Via CLI

```bash
npm install -g netlify-cli
cd /path/to/seyi-growth
netlify deploy --prod
```

---

## 📋 Deployment Checklist

Before going live, make sure you've:

- [ ] Updated all text content (headline, services, pricing)
- [ ] Replaced portfolio case studies with real projects
- [ ] Added real client testimonials
- [ ] Updated contact email and phone number
- [ ] Updated social media links
- [ ] Set up custom domain
- [ ] Tested site on mobile and desktop
- [ ] Added Google Analytics (optional)
- [ ] Set up contact form backend (optional)

---

## 🔄 Making Updates After Deployment

Every time you update your code:

```bash
# Make changes to files
# Then commit and push:
git add .
git commit -m "Update: describe what changed"
git push origin main
```

Vercel/Netlify will automatically rebuild and deploy your changes.

---

## 📊 Set Up Google Analytics (Optional)

1. Go to [analytics.google.com](https://analytics.google.com)
2. Create a new property for your domain
3. Get your Measurement ID (looks like `G-XXXXXXXXXX`)
4. Add to `app/layout.tsx`:

```tsx
import Script from 'next/script';

export default function RootLayout({ children }) {
  return (
    <html>
      <head>
        <Script
          strategy="lazyOnload"
          src={`https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX`}
        />
        <Script strategy="lazyOnload">
          {`
            window.dataLayer = window.dataLayer || [];
            function gtag(){dataLayer.push(arguments);}
            gtag('js', new Date());
            gtag('config', 'G-XXXXXXXXXX');
          `}
        </Script>
      </head>
      <body>{children}</body>
    </html>
  );
}
```

---

## 🔌 Set Up Contact Form Backend (Optional)

### Option 1: FormSubmit (Easiest, Free)

1. In `components/Contact.tsx`, change form action:

```tsx
<form action="https://formsubmit.co/your-email@example.com" method="POST">
  {/* Your form fields */}
</form>
```

2. First submission will ask you to confirm - check your email

### Option 2: Supabase (Recommended for Production)

1. Create account at [supabase.com](https://supabase.com)
2. Create a new project
3. Create a table for form submissions
4. Get your API credentials
5. Add to `.env.local`:

```
NEXT_PUBLIC_SUPABASE_URL=your_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_key
```

6. Create an API route in `app/api/contact/route.ts` to handle submissions

---

## 🐛 Troubleshooting

### Build fails on Vercel

1. Check the build logs on Vercel dashboard
2. Common issues:
   - Missing dependencies: run `npm install`
   - TypeScript errors: fix them locally with `npm run build`
   - Environment variables: add them in Vercel dashboard

### Site looks broken after deployment

1. Check that all images/assets are in `public/` folder
2. Clear browser cache (Cmd+Shift+R or Ctrl+Shift+R)
3. Check browser console for errors

### Contact form not working

1. Make sure form backend is configured
2. Check email is correct
3. Test locally first: `npm run dev`

---

## 📞 Support

Need help? Check:
- [Next.js Docs](https://nextjs.org/docs)
- [Vercel Docs](https://vercel.com/docs)
- [Netlify Docs](https://docs.netlify.com)

---

**Happy deploying! 🚀**
