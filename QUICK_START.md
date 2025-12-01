# 🚀 InstaOrder - Quick Start (60 Seconds)

**Zero Pasting Required!** Uses Cursor Copilot to auto-generate everything.

## 3 Steps to Running InstaOrder

### 1️⃣ Clone the Repo
```bash
git clone https://github.com/el-maximo/instaorder.git
cd instaorder
npm install
```

### 2️⃣ Generate All Files with Cursor Copilot

1. Open Cursor IDE
2. File → Open Folder → select `instaorder`
3. Press **Cmd+K** (Mac) or **Ctrl+K** (Windows)
4. Paste the prompt from `COPILOT_GUIDE.md`
5. Wait 2-3 minutes for Copilot to generate all files
6. Review the generated files in your editor

### 3️⃣ Run the Application

**Terminal 1:**
```bash
npm run dev
```
Open http://localhost:5173

**Terminal 2:**
```bash
npm run server
```

✅ **Done!** Your food ordering system is live.

## What You Get

```
✨ React 18 + TypeScript + Tailwind UI
📦 Shopping cart with quantity controls
💳 Checkout modal with customer details
🔌 Express backend with API endpoints
📱 Fully responsive design
🍕 Ready for Petpooja integration
```

## File Generation

Copilot will generate:
```
src/
├── types.ts          # TypeScript interfaces
├── cartStore.tsx     # Cart state management
├── App.tsx          # React components (Menu, Cart, Checkout)
├── index.css        # Tailwind styles
└── main.tsx         # React entry point

server/
└── index.ts         # Express API server

vite.config.ts       # Vite configuration
tailwind.config.js   # Tailwind theme
tsconfig.json        # TypeScript config
postcss.config.js    # PostCSS configuration
```

## Features

- **Menu Page**: Browse products with images & prices
- **Add to Cart**: One-click adding with auto-incrementing
- **Cart Drawer**: Fixed sidebar showing items & total
- **Quantity Controls**: +/- buttons per item
- **Checkout**: Modal with name, phone, address
- **Order Submission**: POST to backend API
- **Success Message**: Shows order ID after placement
- **Responsive**: Works on mobile, tablet, desktop
- **Tailwind Styled**: Professional emerald green theme

## API Endpoints

```bash
GET  http://localhost:4000/api/menu
POST http://localhost:4000/api/orders
```

## Next Steps

1. ✅ Test the UI locally
2. ✅ Connect to real database
3. ✅ Integrate Petpooja POS API
4. ✅ Add Razorpay/payment gateway
5. ✅ Deploy to production

## Need Help?

- **Stuck on Copilot?** → Read `COPILOT_GUIDE.md`
- **Want more details?** → Check `README.md`
- **Errors in generated code?** → Ask Copilot to fix it
  - Example: "Fix the App.tsx file, the checkout button isn't working"

## One More Thing

No pasting code = faster setup = more time coding! 🎉

The entire system is generated in minutes using Cursor's AI, not manual copy-paste.
