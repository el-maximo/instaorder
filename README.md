# InstaOrder - Food Ordering System

Complete React + TypeScript + Tailwind food ordering system with Petpooja POS integration.

## Quick Setup (No Pasting Required!)

Instead of manual file creation, use this approach:

### Option 1: Clone & Setup (Recommended)

```bash
git clone https://github.com/el-maximo/instaorder.git
cd instaorder

# Install dependencies
npm install

# Run development server
npm run dev
```

### Option 2: Use Cursor IDE with Copilot

1. Open Cursor IDE
2. Clone: `git clone https://github.com/el-maximo/instaorder.git`
3. Open folder in Cursor
4. Use Copilot Chat: Cmd+K and ask:
   ```
   Generate all files for React food ordering system with:
   - src/types.ts (Product, CartItem, OrderRequest interfaces)
   - src/cartStore.tsx (React Context for cart management)
   - src/App.tsx (Menu, ProductCard, CartDrawer, CheckoutModal components)
   - server/index.ts (Express API with /api/menu and /api/orders endpoints)
   - vite.config.ts configuration
   - tailwind.config.js configuration
   Using production-ready code with proper error handling and Tailwind styling.
   ```
5. Cursor will generate all files automatically

### Option 3: Via Cursor Agents (Future)

Once Cursor Agents is stable, submit a build request in the Agents dashboard.

## Project Structure

```
instaorder/
├── src/
│   ├── types.ts           # TypeScript interfaces
│   ├── cartStore.tsx      # React Context cart state
│   ├── App.tsx            # Main React component
│   ├── index.css          # Tailwind imports
│   └── main.tsx           # Entry point
├── server/
│   └── index.ts           # Express backend
├── package.json           # Dependencies
├── vite.config.ts         # Vite config
├── tailwind.config.js     # Tailwind config
└── tsconfig.json          # TypeScript config
```

## Features

✅ **Frontend**
- React 18 + TypeScript + Tailwind CSS
- Menu browsing with product grid
- Shopping cart with quantity controls
- Checkout modal with customer details
- Real-time totals and notifications
- Responsive design (mobile, tablet, desktop)

✅ **Backend**
- Express API server
- GET /api/menu - Fetch products
- POST /api/orders - Submit orders
- Error handling & validation
- Ready for Petpooja integration

✅ **State Management**
- React Context API for cart
- No Redux - lightweight & simple
- TypeScript interfaces for type safety

## Installation

```bash
npm install
```

## Development

```bash
# Start frontend (port 5173)
npm run dev

# Start backend (port 4000 in separate terminal)
npm run server
```

## Build

```bash
npm run build
```

## API Endpoints

### GET /api/menu
Fetch all available products.

**Response:**
```json
[
  {
    "id": "p1",
    "petpoojaItemId": "PIZZA_001",
    "name": "Margherita Pizza",
    "price": 249,
    "description": "Fresh mozzarella and basil",
    "image": "https://..."
  }
]
```

### POST /api/orders
Create a new order.

**Request:**
```json
{
  "customerName": "John Doe",
  "customerPhone": "9876543210",
  "address": "123 Main St",
  "items": [
    {
      "id": "p1",
      "petpoojaItemId": "PIZZA_001",
      "name": "Margherita Pizza",
      "price": 249,
      "quantity": 2
    }
  ]
}
```

**Response:**
```json
{
  "success": true,
  "externalOrderId": "uuid-here"
}
```

## Petpooja Integration

To connect to Petpooja:

1. Get API credentials from Petpooja partner portal
2. Add to `.env`:
   ```
   PETPOOJA_API_URL=https://api.petpooja.com
   PETPOOJA_API_KEY=your_api_key
   PETPOOJA_OUTLET_ID=your_outlet_id
   ```
3. Update `server/index.ts` POST `/api/orders` to call Petpooja API

## Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS, Vite
- **Backend**: Node.js, Express, TypeScript
- **State**: React Context API
- **POS**: Petpooja (integration ready)

## Next Steps

1. Clone the repo
2. Run `npm install`
3. Use Cursor Copilot to generate all source files
4. Run `npm run dev` for frontend
5. Run `npm run server` for backend in another terminal
6. Open http://localhost:5173

## License

MIT
