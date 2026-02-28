# SEIN Clothing Website

A minimalist e-commerce website with shopping cart, admin dashboard, and dark mode.

---

## 🚀 Quick Start

### 1. Install Dependencies
```bash
npm install
```

### 2. Setup Environment (already done!)
The `.env` file is included with the database path.

### 3. Initialize Database
```bash
npx prisma db push
```

### 4. Run Development Server
```bash
npm run dev
```

### 5. Open Browser
Go to: http://localhost:3000

---

## 🔐 Admin Access

- **URL**: http://localhost:3000/admin-login
- **Password**: `Sein@Admin2024!Secure`

⚠️ **Change the password before deploying!** Edit `src/lib/store.ts` line 120.

---

## 📁 File Structure

```
src/
├── app/                    # Pages
│   ├── page.tsx           # Homepage (/)
│   ├── shop/              # Shop page (/shop)
│   ├── product/[id]/      # Product detail (/product/1)
│   ├── about/             # About page (/about)
│   ├── contact/           # Contact page (/contact)
│   ├── checkout/          # Checkout (/checkout)
│   ├── admin/             # Admin dashboard (/admin)
│   ├── admin-login/       # Admin login (/admin-login)
│   └── api/               # Backend APIs
│
├── components/
│   ├── header.tsx         # Navigation header
│   ├── footer.tsx         # Footer with newsletter
│   ├── cart-drawer.tsx    # Shopping cart
│   ├── admin-dashboard.tsx # Admin panel
│   ├── sections/          # Homepage sections
│   └── ui/                # UI components
│
├── lib/
│   ├── store.ts           # State management (cart, admin)
│   ├── products.ts        # Product data
│   ├── db.ts              # Database client
│   └── utils.ts           # Utilities
│
└── hooks/
    └── use-toast.ts       # Toast notifications

prisma/
└── schema.prisma          # Database schema

public/
├── favicon.svg            # Site favicon
├── logo.svg               # Logo
└── robots.txt             # SEO
```

---

## 🎨 Customization

### Change Colors
Edit `src/app/globals.css`:
```css
:root {
  --olive: #5C6B4A;    /* Primary color */
  --cream: #F5F0E8;    /* Background */
  --charcoal: #2A2A2A; /* Text */
}
```

### Change Products
Edit `src/lib/products.ts` or use Admin Dashboard at `/admin`.

### Change Contact Info
Edit `src/components/footer.tsx` and `src/app/contact/page.tsx`.

### Change Logo
Edit `src/components/header.tsx` and `src/components/footer.tsx`.

---

## 🗄️ Database Commands

```bash
# Push schema changes
npx prisma db push

# View database
npx prisma studio

# Reset database
npx prisma db push --force-reset
```

---

## 📦 Build for Production

```bash
npm run build
npm start
```

---

## 🔧 Troubleshooting

### "Module not found"
```bash
rm -rf node_modules
npm install
```

### "Database error"
```bash
npx prisma db push --force-reset
```

### TypeScript errors in VS Code
1. Run `npm install`
2. Press `Ctrl+Shift+P` → "TypeScript: Restart TS Server"

---

## 📞 Pages

| Page | URL |
|------|-----|
| Homepage | `/` |
| Shop | `/shop` |
| Product | `/product/1` |
| About | `/about` |
| Contact | `/contact` |
| Checkout | `/checkout` |
| Admin Login | `/admin-login` |
| Admin Dashboard | `/admin` |

---

## 🛒 Features

- ✅ Shopping cart (localStorage)
- ✅ Product filtering by category
- ✅ Dark/light mode
- ✅ Admin dashboard
- ✅ Order management
- ✅ Newsletter signup
- ✅ Mobile responsive

---

## 📷 Images

All product images use Unsplash URLs (external). To use your own images:
1. Add images to `public/images/` folder
2. Update image URLs in `src/lib/products.ts`

---

**Admin Password**: `Sein@Admin2024!Secure`

Built with Next.js 16, TypeScript, Tailwind CSS, and shadcn/ui.
