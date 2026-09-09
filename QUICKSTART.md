# Quick Start Guide - Seyi Growth

Get your website up and running in 5 minutes.

## ⚡ 5-Minute Setup

### 1. Clone the repository (1 minute)

```bash
git clone https://github.com/Chris26creators/seyi-growth.git
cd seyi-growth
```

### 2. Install and run (2 minutes)

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) 🎉

### 3. Customize essentials (2 minutes)

Edit these files immediately:

**`app/layout.tsx`** - Change title and description
```tsx
title: 'YOUR NAME | YOUR MAIN SERVICE',
description: 'What you do...',
```

**`components/Contact.tsx`** - Add your email
```tsx
hello@seyigrowth.com  ➜  your-email@example.com
```

**`components/Hero.tsx`** - Update headline
```tsx
"Turn Your Store Into a Sales Machine" ➜ "Your headline here"
```

---

## 📝 Next: Customize Your Content

### Update Services (5 minutes)
Edit: `components/Services.tsx`
- Change service titles and descriptions
- Keep or replace icons

### Update Portfolio (10 minutes)
Edit: `components/Portfolio.tsx`
- Replace example case studies with YOUR projects
- Update metrics and results

### Update Pricing (5 minutes)
Edit: `components/Pricing.tsx`
- Change prices and package names
- Update features list

### Update Testimonials (5 minutes)
Edit: `components/Testimonials.tsx`
- Add real client quotes
- Update author names and roles

---

## 🚀 Deploy in 3 Steps

### Step 1: Push to GitHub

```bash
git remote add origin https://github.com/Chris26creators/seyi-growth.git
git branch -M main
git push -u origin main
```

### Step 2: Deploy to Vercel

1. Go to [vercel.com](https://vercel.com)
2. Click "Add New Project"
3. Select your GitHub repository
4. Click "Deploy"

**Your website is now LIVE!** 🎉

### Step 3: Add Custom Domain (Optional)

1. In Vercel, go to Settings → Domains
2. Add your domain
3. Update DNS (Vercel will guide you)

---

## 📚 Full Guides

- **README.md** - Overview and features
- **CUSTOMIZATION.md** - Detailed customization examples
- **DEPLOYMENT.md** - Complete deployment guide
- **QUICKSTART.md** - This file (quick setup)

---

## 🔗 Useful Links

- [Next.js Docs](https://nextjs.org/docs)
- [Tailwind CSS](https://tailwindcss.com)
- [Framer Motion](https://www.framer.com/motion)
- [React Icons](https://react-icons.github.io/react-icons)
- [Vercel Docs](https://vercel.com/docs)

---

## ✅ Checklist Before Launching

- [ ] All text updated
- [ ] Contact email added
- [ ] Portfolio cases added
- [ ] Testimonials updated
- [ ] Pricing set
- [ ] Tested on mobile
- [ ] Pushed to GitHub
- [ ] Deployed to Vercel
- [ ] Custom domain added
- [ ] Links tested

---

## 🆘 Quick Troubleshooting

**npm install fails?**
```bash
npm install --legacy-peer-deps
```

**Port 3000 already in use?**
```bash
npm run dev -- -p 3001
```

**Build errors?**
```bash
rm -rf .next
npm run build
```

**Deploy shows old content?**
- Clear Vercel cache: Project Settings → Deployments → Clear Cache & Redeploy

---

## 💡 Pro Tips

1. **Test locally first**: Always run `npm run dev` before pushing
2. **Git regularly**: Commit often with clear messages
3. **One change at a time**: Easier to debug if something breaks
4. **Backup your customizations**: Keep a copy of your content
5. **Mobile first**: Test on phone before sharing

---

**You're ready to go! Happy building! 🚀**

For more details:
- See **CUSTOMIZATION.md** for detailed examples
- See **DEPLOYMENT.md** for production setup
