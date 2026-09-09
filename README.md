# Seyi Growth - E-commerce & Services Portfolio Website

A modern, responsive portfolio website for freelance e-commerce specialists and service providers. Built with **Next.js 14**, **TypeScript**, **Tailwind CSS**, and **Framer Motion**.

## 🎯 Features

- ✨ **Modern Design** - Clean, professional aesthetics with smooth animations
- 📱 **Fully Responsive** - Works perfectly on mobile, tablet, and desktop
- ⚡ **Fast Performance** - Optimized for speed and SEO
- 🎨 **Beautiful Components** - Hero, Services, Portfolio, Testimonials, Pricing, Contact
- 📊 **Easy to Customize** - Well-organized code, easy to update content
- 🚀 **Production Ready** - Deploy to Vercel, Netlify, or any hosting

## 📋 Quick Start

### Prerequisites
- Node.js 18.17 or later
- npm or yarn

### Installation

```bash
# Clone repository
git clone https://github.com/Chris26creators/seyi-growth.git
cd seyi-growth

# Install dependencies
npm install

# Run development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see your site.

## 🎨 Customization Guide

### 1. Update Your Information

**File: `app/layout.tsx`**
- Change the site title, description, and keywords
- Update OpenGraph tags for social sharing

### 2. Edit Components

Each component is in the `components/` folder:
- `Header.tsx` - Navigation and logo
- `Hero.tsx` - Main headline and CTA
- `Services.tsx` - Your services list
- `Portfolio.tsx` - Case studies and projects
- `Process.tsx` - How you work
- `Testimonials.tsx` - Client reviews
- `Pricing.tsx` - Your pricing plans
- `Contact.tsx` - Contact form and info
- `Footer.tsx` - Footer links

### 3. Update Content

**Services** (`components/Services.tsx`):
```tsx
const services = [
  {
    title: 'Your Service Name',
    description: 'What you do...',
    icon: ShoppingCart,
    color: 'from-blue-400 to-blue-600',
  },
  // Add more...
];
```

**Portfolio Cases** (`components/Portfolio.tsx`):
```tsx
const caseStudies = [
  {
    title: 'Client Project Name',
    results: [
      { metric: '+68%', label: 'Conversion Rate' },
    ],
  },
];
```

**Pricing** (`components/Pricing.tsx`):
Update the plans array with your pricing and features.

**Contact** (`components/Contact.tsx`):
- Update email: `hello@seyigrowth.com`
- Update phone: `+234 912 451 6242`
- Update WhatsApp link

### 4. Change Colors

Edit `app/globals.css` or `tailwind.config.ts` to change the color scheme from blue to your preferred color.

## 🌐 Deploy to Production

### Deploy to Vercel (Easiest)

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

Or:
1. Push to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Click Deploy

### Deploy to Netlify

```bash
npm i -g netlify-cli
netlify deploy --prod
```

### Custom Domain

After deploying:
1. Point your domain's DNS to your hosting provider
2. Add the domain in your Vercel/Netlify dashboard

## 📁 Project Structure

```
seyi-growth/
├── app/
│   ├── layout.tsx          # Root layout & metadata
│   ├── page.tsx            # Home page
│   └── globals.css         # Global styles
├── components/             # All React components
│   ├── Header.tsx
│   ├── Hero.tsx
│   ├── Services.tsx
│   ├── Portfolio.tsx
│   ├── Process.tsx
│   ├── Testimonials.tsx
│   ├── Pricing.tsx
│   ├── Contact.tsx
│   └── Footer.tsx
├── public/                 # Static files
└── package.json            # Dependencies
```

## 🔧 Available Scripts

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm start        # Start production server
npm run lint     # Run ESLint
```

## 💡 Tips

- All animations use Framer Motion - smooth and performant
- Icons from `react-icons` - easy to swap
- Fully typed with TypeScript - no `any` types
- Mobile-first responsive design
- SEO optimized metadata
- Contact form ready for Supabase integration

## ✨ Next Steps After Deploying

1. Add Google Analytics
2. Set up form backend (Supabase, FormSubmit, etc.)
3. Add real images and case studies
4. Get domain name
5. Share on social media

## 📞 Questions?

Check each component file - they have clear comments explaining what to customize.

---

**Happy building! 🚀**

Made for entrepreneurs building their service business online.
