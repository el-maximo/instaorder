# InstaOrder - Cursor Copilot Setup Guide

## 🎯 Generate All Files Using Cursor Copilot (NO PASTING!)

This is the fastest way to build the entire InstaOrder system without manually pasting code.

## Step 1: Clone the Repository

```bash
git clone https://github.com/el-maximo/instaorder.git
cd instaorder
```

## Step 2: Open in Cursor IDE

1. Open Cursor IDE
2. Click "File" → "Open Folder"
3. Select the `instaorder` folder

## Step 3: Use Copilot to Generate Files

### Open Copilot Chat
- **Mac**: `Cmd + K`
- **Windows/Linux**: `Ctrl + K`

### Paste This Prompt

Copy and paste the entire prompt below into Copilot:

```
Generate complete InstaOrder food ordering system files with React + TypeScript + Tailwind.

1) Create src/types.ts with:
   - Product interface: id, petpoojaItemId, name, price, image, description
   - CartItem extends Product with quantity
   - OrderRequest with customerName, customerPhone, address, items, notes
   - Order extends OrderRequest with externalOrderId and timestamp

2) Create src/cartStore.tsx with:
   - CartContext using React.createContext
   - CartProvider component with useState
   - useCart hook
   - Methods: addToCart, removeFromCart, updateQty, clearCart
   - Calculate total price

3) Create src/App.tsx with:
   - ProductCard component showing image, name, description, price, add button
   - CartDrawer component showing items with +/- qty controls, delete, total, checkout button
   - CheckoutModal component with name/phone/address inputs, success/error messages
   - MenuPage component that fetches /api/menu and displays products
   - Responsive Tailwind styling with emerald green theme
   - All components use proper error handling

4) Create server/index.ts Express server with:
   - GET /api/menu endpoint returning array of mock products
   - Products include: Margherita Pizza, Farmhouse Pizza, Garlic Bread, Coke
   - POST /api/orders endpoint accepting OrderRequest
   - Generate UUID for externalOrderId
   - Mock Petpooja integration (ready for real API)
   - CORS enabled
   - Port 4000

5) Create vite.config.ts with React plugin and proxy to http://localhost:4000/api

6) Create tailwind.config.js with content paths and theme colors

7) Create tsconfig.json for React + DOM + Node

8) Create postcss.config.js

9) Create src/index.css with Tailwind directives

10) Create src/main.tsx entry point mounting App to root

Use production-ready code with:
- Proper TypeScript types everywhere
- Error handling and validation
- Tailwind CSS for all styling
- Responsive mobile-first design
- Loading states
- Success/error notifications
- Modern React patterns (hooks, context)
```

## Step 4: Review Generated Files

After Copilot generates all files, review them:

```bash
ls -la src/
ls -la server/
```

Expected files:
```
src/
├── types.ts
├── cartStore.tsx
├── App.tsx
├── index.css
├── main.tsx
└── (vite app defaults)

server/
└── index.ts

Root:
├── vite.config.ts
├── tailwind.config.js
├── postcss.config.js
├── tsconfig.json
├── package.json
└── README.md
```

## Step 5: Install Dependencies

```bash
npm install
```

## Step 6: Run the Application

### Terminal 1 - Frontend
```bash
npm run dev
```

Open http://localhost:5173

### Terminal 2 - Backend
```bash
npm run server
```

## Step 7: Test the App

1. Browse menu items
2. Click "Add" to add items to cart
3. Modify quantities with +/- buttons
4. Click "Checkout"
5. Fill in name, phone, address
6. Click "Order Now"
7. See success message with order ID

## Troubleshooting

### "Cannot find module"
```bash
rm -rf node_modules package-lock.json
npm install
```

### Port already in use
```bash
# Frontend on different port
npm run dev -- --port 3000

# Backend on different port
# Edit server/index.ts and change port
```

### CORS errors
- Make sure backend is running on port 4000
- Vite proxy should redirect /api to localhost:4000

## Next Steps

1. **Database**: Add MongoDB/PostgreSQL for products and orders
2. **Auth**: Add customer login/registration
3. **Petpooja Integration**: Replace mock endpoint with real Petpooja API
4. **Payments**: Add Razorpay/Stripe integration
5. **Admin Panel**: Build order management dashboard
6. **Mobile App**: Create React Native version

## Copilot Tips

- If Copilot doesn't generate a file, ask: "Create the [filename] file with..."
- For fixes: "Fix the [filename] file, it should..."
- For changes: "Update [filename] to include..."
- Copy entire error messages into Copilot for debugging
- Use Ctrl+L to clear chat history and start fresh

## Support

If files aren't generated correctly:

1. Try asking Copilot: "Generate TypeScript interfaces for Product and CartItem"
2. Then ask: "Generate React Context for cart management"
3. Break down into smaller requests if needed
4. Check Cursor's Copilot logs (View → Output)
