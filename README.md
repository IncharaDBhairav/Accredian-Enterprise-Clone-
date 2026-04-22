# Accredian Enterprise Clone

A modern, fully-responsive Next.js landing page clone for Accredian Enterprise. Built with Next.js 14, Tailwind CSS, and TypeScript for optimal performance and developer experience.

## 🎯 Features

- **Responsive Design**: Mobile-first approach, optimized for all devices
- **Sticky Navigation Bar**: Smooth scrolling with dynamic styling
- **Multiple Landing Sections**: Hero, Stats, Programs, How it Works, and Contact
- **Lead Capture Form**: Fully functional contact form with validation
- **API Integration**: Mock API route for lead submissions at `/api/lead`
- **Reusable Components**: Clean, modular component architecture
- **Type-Safe**: Full TypeScript support with interfaces for better DX
- **Performance Optimized**: Vercel-ready with next/image optimization

## 📁 Project Structure

```
Accredian Clone/
├── app/                          # Next.js App Router
│   ├── api/lead/route.ts        # Lead submission API endpoint
│   ├── layout.tsx               # Root layout with Navbar & Footer
│   └── page.tsx                 # Main landing page
├── components/
│   ├── common/                  # Shared components
│   │   ├── Navbar.tsx          # Sticky navigation bar
│   │   ├── Footer.tsx          # Footer component
│   │   └── SectionHeader.tsx    # Reusable section header
│   ├── sections/                # Page sections
│   │   ├── HeroSection.tsx      # Hero banner with CTA
│   │   ├── StatsSection.tsx     # Impact statistics
│   │   ├── ProgramGridSection.tsx # Program listings
│   │   ├── HowItWorksSection.tsx  # Process steps
│   │   └── ContactFormSection.tsx # Lead capture form
│   └── ui/                      # UI primitives
│       ├── Button.tsx           # Reusable button component
│       ├── Card.tsx             # Card wrapper component
│       └── FormInput.tsx         # Form input field
├── styles/
│   └── globals.css              # Global Tailwind styles
├── types/
│   └── index.ts                 # TypeScript interfaces
├── public/                      # Static assets
├── package.json                 # Dependencies
├── tailwind.config.ts           # Tailwind configuration
├── tsconfig.json                # TypeScript configuration
├── next.config.js               # Next.js configuration
└── postcss.config.js            # PostCSS configuration
```

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or yarn package manager

### Installation

1. Navigate to the project directory:
```bash
cd "Accredian Clone"
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## 📝 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm start` - Run production server
- `npm run lint` - Run ESLint

## 🎨 Component Library

### Reusable Components

#### Button
```tsx
<Button 
  variant="primary" // primary | secondary | outline | ghost
  size="md"         // sm | md | lg
  onClick={handleClick}
>
  Click Me
</Button>
```

#### Card
```tsx
<Card hover className="custom-class">
  <p>Card content here</p>
</Card>
```

#### FormInput
```tsx
<FormInput 
  label="Email"
  name="email"
  type="email"
  error={errors.email}
  required
  onChange={handleChange}
/>
```

#### SectionHeader
```tsx
<SectionHeader
  title="Section Title"
  subtitle="Optional subtitle"
  centered={true}
/>
```

## 📡 API Routes

### POST `/api/lead`
Handles lead form submissions

**Request Body:**
```json
{
  "name": "John Doe",
  "email": "john@company.com",
  "phone": "+1 (555) 123-4567",
  "company": "Company Name",
  "employees": "501-1000",
  "interest": "Leadership"
}
```

**Success Response:**
```json
{
  "success": true,
  "message": "Thank you for your interest!",
  "data": { ... }
}
```

**Error Response:**
```json
{
  "success": false,
  "message": "Validation error message"
}
```

## 🎨 Tailwind Configuration

The project uses custom color extensions:
- `primary`: `#1e40af` (Blue)
- `secondary`: `#0f766e` (Teal)
- `accent`: `#ea580c` (Orange)

Customize colors in `tailwind.config.ts`

## 🔧 Customization

### Update Branding
Edit the logo and brand name in `components/common/Navbar.tsx` and `components/common/Footer.tsx`

### Modify Colors
Update the color palette in `tailwind.config.ts`:
```ts
colors: {
  primary: '#your-color',
  secondary: '#your-color',
  accent: '#your-color',
}
```

### Replace Content
- Update program listings in `components/sections/ProgramGridSection.tsx`
- Modify stats in `components/sections/StatsSection.tsx`
- Customize steps in `components/sections/HowItWorksSection.tsx`

### Connect Real API
Replace the mock implementation in `app/api/lead/route.ts` with:
- Database integration (PostgreSQL, MongoDB, etc.)
- Email service (SendGrid, Mailgun, etc.)
- CRM integration (HubSpot, Salesforce, etc.)

## 📱 Responsive Breakpoints

Built-in Tailwind breakpoints:
- `sm`: 640px
- `md`: 768px
- `lg`: 1024px
- `xl`: 1280px
- `2xl`: 1536px

## 🔐 Security Considerations

- Form validation on both client and server
- Input sanitization in API routes
- CORS handling for API endpoints
- Sensitive data handling in environment variables

## 🚀 Deployment

### Deploy to Vercel
```bash
npm install -g vercel
vercel
```

### Build for Production
```bash
npm run build
npm start
```

## 📚 Documentation & Resources

- [Next.js Docs](https://nextjs.org/docs)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [React Documentation](https://react.dev)
- [TypeScript Handbook](https://www.typescriptlang.org/docs)

## 🤝 Contributing

When making improvements:
1. Keep components focused and modular
2. Use TypeScript for type safety
3. Follow the existing code style
4. Document complex logic with comments
5. Test responsive design across breakpoints

## 📝 Notes

- This is a partial clone focusing on the landing page
- The contact form is fully functional but uses mock API (replace in production)
- All icons use inline SVGs for better performance
- Mobile menu auto-closes when navigating

## 📄 License

This project is for educational purposes. Accredian is a trademark of its respective owners.

---

**Created with ❤️ using Next.js, Tailwind CSS, and TypeScript**
