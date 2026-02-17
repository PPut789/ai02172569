# PHaveCPU E-Commerce Website Specification

## 1. Project Overview

**Project Name:** PHaveCPU - Premium Computer & Gaming Gear Store
**Project Type:** Single-Page E-Commerce Application
**Core Functionality:** A high-end storefront for gaming hardware featuring dynamic product filtering, shopping cart, and simulated checkout
**Target Users:** PC gamers, hardware enthusiasts, and custom PC builders

---

## 2. UI/UX Specification

### Layout Structure

**Page Sections:**
- Sticky Header (80px height)
- Hero Carousel (600px height)
- Filter Sidebar + Product Grid (Main Shop Area)
- Footer (4-column layout)

**Responsive Breakpoints:**
- Desktop: ≥1024px (4-column grid, sidebar visible)
- Tablet: 768px-1023px (2-column grid, collapsible sidebar)
- Mobile: <768px (1-column grid, hamburger menu)

### Visual Design

**Color Palette:**
- Primary Red: `#E11D48` (Rose-600)
- Primary Red Hover: `#BE123C` (Rose-700)
- Secondary White: `#FFFFFF`
- Background Light: `#F9FAFB` (Gray-50)
- Background Dark: `#111827` (Gray-900)
- Text Primary: `#111827` (Gray-900)
- Text Secondary: `#6B7280` (Gray-500)
- Border: `#E5E7EB` (Gray-200)
- Glow Effect: `rgba(225, 29, 72, 0.4)`

**Typography:**
- Headings: 'Orbitron', sans-serif (Google Fonts) - Tech/Gaming aesthetic
- Body: 'Inter', sans-serif (Google Fonts)
- Logo: 'Orbitron' Bold, 28px
- H1: 48px / 56px (mobile: 32px)
- H2: 36px / 44px
- H3: 24px / 32px
- Body: 16px / 24px
- Small: 14px / 20px

**Spacing System:**
- Section padding: 80px vertical (mobile: 48px)
- Container max-width: 1280px
- Grid gap: 24px
- Card padding: 20px

**Visual Effects:**
- Card hover: translateY(-8px) + box-shadow glow
- Button hover: scale(1.05) + glow effect
- Transitions: all 0.3s ease
- Modal backdrop: rgba(0, 0, 0, 0.6)

### Components

**1. Header/Navigation:**
- Fixed position, z-index 50
- Background: White with subtle shadow on scroll
- Logo (left): "PHaveCPU" in Orbitron, red color
- Nav links (center): Home, All Products, Promotions, Contact
- Icons (right): Search icon, Cart icon with badge counter
- Mobile: Hamburger menu

**2. Hero Carousel:**
- Full-width, 600px height
- Auto-play every 5 seconds
- 3 slides with gradient overlays
- Navigation dots at bottom
- "Shop Now" CTA button

**3. Filter Sidebar:**
- Width: 280px (desktop)
- Sticky position
- Price Range Slider (dual handle)
- Category Checkboxes
- "Apply Filters" button
- "Clear All" link

**4. Product Card:**
- Aspect ratio image container (4:3)
- Product image with hover zoom
- Category badge
- Product title (2-line truncate)
- Price (red, bold)
- "Add to Cart" button
- "View Details" button
- Hover: lift + glow effect

**5. Product Detail Modal:**
- Centered modal (max-width: 900px)
- Large product image (left)
- Product details (right): title, category, price, description, specs
- Quantity selector
- "Add to Cart" + "Buy Now" buttons
- Close button (X)

**6. Cart Drawer:**
- Slides from right
- Overlay backdrop
- Item list with quantity controls
- Remove item button
- Subtotal calculation
- "Checkout" button

**7. Checkout Page:**
- Full-width section
- Form fields: Name, Email, Address, Card Number
- Order summary sidebar
- "Confirm Payment" button
- Loading spinner on payment

**8. Success Screen:**
- Full-screen overlay
- Animated checkmark
- "Order Confirmed!" message
- Order summary
- "Continue Shopping" button

**9. Footer:**
- 4-column grid (desktop)
- Quick Links, Categories, Contact Info, Newsletter
- Social media icons
- Copyright text

---

## 3. Functionality Specification

### Core Features

**Product Data:**
- 12 mock products across 4 categories
- Categories: Laptops, Custom PC Sets, Components, Gaming Gear
- Data: id, name, category, price, image, description, specs

**Filtering System:**
- Price range: $0 - $5000
- Category multi-select
- Real-time filtering (no page reload)
- Results count display

**Shopping Cart:**
- Add to cart functionality
- Quantity adjustment (+/-)
- Remove item
- Persistent cart (localStorage)
- Cart badge counter
- Subtotal calculation

**Checkout Flow:**
- Form validation (required fields)
- Simulated payment processing (2s delay)
- Success animation
- Cart clear on success
- Redirect to home

### User Interactions

1. **Browse Products:** Scroll through grid, use filters
2. **View Details:** Click "View Details" → Modal opens
3. **Add to Cart:** Click button → Cart badge updates, drawer opens
4. **Manage Cart:** Adjust quantities, remove items
5. **Checkout:** Fill form → Confirm → Success animation
6. **Navigation:** All links functional with smooth scroll/transition

### Image Sources

Using Unsplash for high-quality tech images:
- Hero: Gaming PC / Liquid cooling images
- Laptops: Gaming laptop images
- Components: CPU/GPU images
- Gaming Gear: Mechanical keyboard, mouse images
- Custom PCs: RGB PC setup images

---

## 4. Acceptance Criteria

### Visual Checkpoints
- [ ] Red/White theme consistently applied
- [ ] Orbitron font for headings
- [ ] Glow effects on hover states
- [ ] Smooth transitions on all interactions
- [ ] Responsive layout works on all breakpoints
- [ ] Product images load correctly

### Functional Checkpoints
- [ ] Carousel auto-plays and navigates
- [ ] Filters update product grid
- [ ] Add to cart updates badge
- [ ] Cart drawer opens/closes
- [ ] Quantity controls work
- [ ] Product modal opens/closes
- [ ] Checkout form validates
- [ ] Success animation displays
- [ ] Cart persists on refresh

### Performance
- [ ] Page loads without console errors
- [ ] Images load progressively
- [ ] Smooth animations (60fps)
