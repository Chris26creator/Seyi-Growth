# Customization Guide - Seyi Growth

Detailed examples and instructions for customizing every part of your website.

## 📝 Site Metadata (SEO)

**File:** `app/layout.tsx`

```tsx
export const metadata: Metadata = {
  title: 'Seyi Growth | Shopify & E-commerce Growth Specialist',
  description:
    'I help businesses increase sales through Shopify store design, website design, branding, SEO, digital marketing, and social media management.',
  keywords:
    'Shopify, E-commerce, Website Design, Branding, SEO, Digital Marketing, Social Media',
  openGraph: {
    title: 'Seyi Growth | Shopify & E-commerce Growth Specialist',
    description: 'Your description here',
    type: 'website',
  },
};
```

**Change these to:**
- `title`: Your name + your main service
- `description`: 160-180 characters describing what you do
- `keywords`: Your services separated by commas
- `openGraph.title` and `description`: For social media sharing

---

## 🎨 Brand Colors

### Option 1: Change throughout with Find & Replace

1. Open any component
2. Find: `blue-` (all blue colors)
3. Replace with: `purple-`, `green-`, `orange-`, etc.
4. Available colors: `blue`, `purple`, `pink`, `red`, `orange`, `green`, `indigo`, `violet`

### Option 2: Update Tailwind Config

**File:** `tailwind.config.ts`

```ts
module.exports = {
  theme: {
    colors: {
      blue: {
        50: '#f0f9ff',
        // ... change these hex values to your brand colors
        600: '#2563eb', // Primary color
      }
    }
  }
}
```

---

## 🏢 Header Customization

**File:** `components/Header.tsx`

```tsx
// Change logo text
<span className="font-bold text-lg text-gray-900">YOUR.NAME</span>

// Update navigation links
const navLinks = [
  { href: '#home', label: 'Home' },
  { href: '#services', label: 'Services' },
  { href: '#portfolio', label: 'Work' },
  { href: '#process', label: 'Process' },
  { href: '#pricing', label: 'Pricing' },
  { href: '#faq', label: 'FAQ' },
];

// Change CTA button text
<Link href="#contact" className="btn-primary text-sm">
  Your CTA Text Here
</Link>
```

---

## 🎯 Hero Section

**File:** `components/Hero.tsx`

```tsx
// Update headline
<h1 className="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
  Turn Your Store Into a{' '}
  <span className="gradient-text">Sales Machine</span>
</h1>

// Update subheading
<p className="text-lg text-gray-600 mb-8 leading-relaxed">
  I help e-commerce brands and small businesses increase visibility,
  engagement, and sales with modern digital marketing strategies.
</p>

// Update statistics
<div className="flex gap-8 mt-12 flex-wrap">
  <div>
    <p className="text-3xl font-bold text-gray-900">50+</p>
    <p className="text-gray-600">Stores Optimized</p>
  </div>
  <div>
    <p className="text-3xl font-bold text-gray-900">$2M+</p>
    <p className="text-gray-600">Revenue Generated</p>
  </div>
  <div>
    <p className="text-3xl font-bold text-gray-900">3x</p>
    <p className="text-gray-600">Avg. Sales Increase</p>
  </div>
</div>
```

---

## 🛠️ Services Section

**File:** `components/Services.tsx`

```tsx
const services = [
  {
    id: 1,
    title: 'Shopify Setup & Design',
    description:
      'Launch your store with a high-converting design. Custom theme setup, product pages, and checkout optimization.',
    icon: ShoppingCart,
    color: 'from-blue-400 to-blue-600',
  },
  // Add or modify services here
];
```

**To add a new service:**

```tsx
{
  id: 7,
  title: 'Your New Service',
  description: 'What you do...',
  icon: YourIcon, // Import from react-icons/fa
  color: 'from-purple-400 to-purple-600',
}
```

**Available icons from react-icons:**
- `ShoppingCart`, `Globe`, `Palette`, `Search`, `TrendingUp`, `Share2`
- Find more at: [react-icons.github.io/react-icons](https://react-icons.github.io/react-icons)

**Color gradients:**
- Blue: `from-blue-400 to-blue-600`
- Purple: `from-purple-400 to-purple-600`
- Pink: `from-pink-400 to-pink-600`
- Green: `from-green-400 to-green-600`
- Orange: `from-orange-400 to-orange-600`

---

## 📸 Portfolio / Case Studies

**File:** `components/Portfolio.tsx`

```tsx
const caseStudies = [
  {
    id: 1,
    title: 'Client Name - Project Type',
    category: 'Shopify Optimization',
    description: 'What you did and how you helped them...',
    results: [
      { metric: '+68%', label: 'Conversion Rate' },
      { metric: '+$2.4K', label: 'Avg Order Value' },
    ],
    image: '👗', // Emoji placeholder
  },
  // Add more...
];
```

**Example with real data:**

```tsx
{
  id: 2,
  title: 'LuxeHome Furniture - E-commerce Optimization',
  category: 'Shopify Setup & Design',
  description: 'Rebuilt entire Shopify store from ground up with modern design and product-focused landing pages. Implemented abandoned cart recovery and email sequences.',
  results: [
    { metric: '+156%', label: 'Conversion Rate' },
    { metric: '+$8.2K', label: 'Monthly Revenue' },
    { metric: '2.4%', label: 'Checkout Conversion' },
  ],
  image: '🛋️',
}
```

**To add images instead of emojis:**

```tsx
// Upload image to public/ folder, e.g., public/project1.jpg
image: '/project1.jpg', // Change from emoji

// Then update component to display it:
<img src={study.image} alt={study.title} className="w-full h-48 object-cover" />
```

---

## 💬 Process Section

**File:** `components/Process.tsx`

```tsx
const steps = [
  {
    number: '01',
    title: 'Discovery Call',
    description:
      'We start with understanding your business, goals, and challenges.',
  },
  {
    number: '02',
    title: 'Strategy & Audit',
    description:
      'I audit your store and competition, then provide a clear roadmap.',
  },
  // Modify as needed
];
```

---

## ⭐ Testimonials

**File:** `components/Testimonials.tsx`

```tsx
const testimonials = [
  {
    id: 1,
    quote:
      '"Their Shopify optimization increased our sales by 300% in 3 months."',
    author: 'John Doe',
    role: 'Founder, Fashion Brand',
    rating: 5,
  },
  // Add real testimonials here
];
```

**Format testimonials professionally:**
- Remove generic praise
- Include specific metrics
- Use real names and businesses
- Focus on tangible results

---

## 💰 Pricing Plans

**File:** `components/Pricing.tsx`

```tsx
const plans = [
  {
    name: 'Starter',
    price: '$450',
    period: 'one-time',
    description: 'Perfect for getting set up properly',
    features: [
      'Feature 1',
      'Feature 2',
      'Feature 3',
    ],
    highlighted: false, // Set to true for featured plan
  },
  // Modify pricing
];
```

**Tips:**
- Set one plan as `highlighted: true` for emphasis
- List benefits in order of importance
- Make prices clear (one-time, monthly, annual)
- Include what each plan does NOT include

---

## 📧 Contact Information

**File:** `components/Contact.tsx`

```tsx
// Update email
<a href="mailto:your-email@example.com">
  your-email@example.com
</a>

// Update WhatsApp
<a href="https://wa.me/1234567890">
  +1 234 567 8900
</a>

// WhatsApp format:
// Replace 1234567890 with your number (country code + number, no spaces)
// Example for Nigeria: https://wa.me/2349124516242
```

**Form fields:**
```tsx
<select name="service">
  <option value="">Select a service</option>
  <option value="shopify-setup">Shopify Setup & Design</option>
  <option value="website-design">Website Design</option>
  <option value="branding">Branding Strategy</option>
  <option value="seo">SEO Optimization</option>
  <option value="digital-marketing">Digital Marketing</option>
  <option value="social-media">Social Media Management</option>
</select>
```

---

## 🔗 Footer

**File:** `components/Footer.tsx`

```tsx
// Update social links
<a href="https://instagram.com/your-handle">
  <Instagram size={20} />
</a>
<a href="https://linkedin.com/in/your-profile">
  <Linkedin size={20} />
</a>
<a href="https://twitter.com/your-handle">
  <Twitter size={20} />
</a>

// Update footer text
<p className="text-sm text-gray-400">
  © 2026 Your Name. All rights reserved.
</p>
```

---

## 🎬 Animations

All components use **Framer Motion** for animations. Modify animation speeds:

**File:** Any component.tsx

```tsx
// Faster animation (0.3 seconds)
transition={{ duration: 0.3 }}

// Slower animation (1 second)
transition={{ duration: 1 }}

// Add delay (0.5 seconds)
transition={{ duration: 0.6, delay: 0.5 }}

// Staggered animations
staggerChildren: 0.1 // Time between each child animation
```

---

## 🔤 Fonts

**File:** `app/layout.tsx`

Current: **Inter** (clean, professional)

**To change fonts:**

```tsx
import { Poppins, Playfair } from 'next/font/google';

// More options:
// - Playfair: Elegant, luxury
// - Montserrat: Modern, bold
// - Raleway: Professional, clean
// - Georgia: Classic, serif
```

---

## 📱 Responsive Design

All components are mobile-first with Tailwind breakpoints:

```tsx
// Mobile-first: applies to all screen sizes
className="text-lg"

// Small screens and up (640px+)
className="sm:text-xl"

// Medium screens and up (768px+)
className="md:text-2xl"

// Large screens and up (1024px+)
className="lg:text-3xl"

// Extra large screens and up (1280px+)
className="xl:text-4xl"
```

---

## 🆘 Common Customizations

### Add a FAQ Section

Create new component: `components/FAQ.tsx`

```tsx
'use client';

const FAQ = () => {
  const faqs = [
    {
      question: 'How long does a Shopify setup take?',
      answer: 'Typically 2-4 weeks depending on product volume.'
    },
    // Add more FAQs
  ];

  return (
    <section id="faq" className="py-20">
      <div className="container-max">
        {faqs.map((faq) => (
          <div key={faq.question}>
            <h3>{faq.question}</h3>
            <p>{faq.answer}</p>
          </div>
        ))}
      </div>
    </section>
  );
};

export default FAQ;
```

Add to `app/page.tsx`:
```tsx
import FAQ from '@/components/FAQ';

export default function Home() {
  return (
    <>
      {/* ... other sections ... */}
      <FAQ />
    </>
  );
}
```

### Add a Blog Section

1. Create `app/blog` folder
2. Add `page.tsx` with blog posts list
3. Create `[slug]/page.tsx` for individual posts

### Add Dark Mode

Update `tailwind.config.ts`:
```ts
module.exports = {
  darkMode: 'class',
}
```

Then add to components:
```tsx
className="bg-white dark:bg-gray-900 text-gray-900 dark:text-white"
```

---

## ✅ Testing Locally

Before deploying, test changes:

```bash
npm run dev
# Visit http://localhost:3000
```

Check:
- [ ] All text displays correctly
- [ ] Images load properly
- [ ] Links work
- [ ] Mobile layout looks good
- [ ] Contact form submits
- [ ] No console errors

---

## 🚀 Quick Reference

| Component | File |
|-----------|------|
| Logo & Navigation | `components/Header.tsx` |
| Main Hero | `components/Hero.tsx` |
| Services | `components/Services.tsx` |
| Case Studies | `components/Portfolio.tsx` |
| How It Works | `components/Process.tsx` |
| Client Reviews | `components/Testimonials.tsx` |
| Plans & Pricing | `components/Pricing.tsx` |
| Contact Form | `components/Contact.tsx` |
| Footer | `components/Footer.tsx` |

---

**Happy customizing! 🎨**
