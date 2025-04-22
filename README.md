# House of CB eCommerce Clone

A full-stack eCommerce application built with Next.js and Strapi CMS, featuring custom clothing measurements, Stripe payments, and user authentication.

## Features

- Next.js 14 with App Router for the frontend
- Strapi CMS for content management
- Custom measurement forms for each product
- Shopping cart with local storage
- User authentication with NextAuth
- Stripe payment integration
- Responsive design with Tailwind CSS
- SEO optimized

## Prerequisites

- Node.js 18+ and npm
- Git
- Stripe account for payments

## Project Structure

```
ecomm/
├── frontend/     # Next.js frontend application
└── backend/      # Strapi CMS backend
```

## Setup Instructions

### Backend (Strapi)

1. Navigate to the backend directory:

   ```bash
   cd backend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the backend directory with the following variables:

   ```
   HOST=0.0.0.0
   PORT=1337
   APP_KEYS=your-app-key-1,your-app-key-2
   API_TOKEN_SALT=your-api-token-salt
   ADMIN_JWT_SECRET=your-admin-jwt-secret
   JWT_SECRET=your-jwt-secret
   STRIPE_SECRET_KEY=your-stripe-secret-key
   ```

4. Start the Strapi server:

   ```bash
   npm run develop
   ```

5. Access the Strapi admin panel at `http://localhost:1337/admin`
   - Create your first admin user
   - Configure permissions for the Product content type
   - Add some products to test the application

### Frontend (Next.js)

1. Navigate to the frontend directory:

   ```bash
   cd frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env.local` file in the frontend directory with the following variables:

   ```
   NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=your-stripe-publishable-key
   STRIPE_SECRET_KEY=your-stripe-secret-key
   NEXTAUTH_URL=http://localhost:3000
   NEXTAUTH_SECRET=your-nextauth-secret
   STRAPI_API_URL=http://localhost:1337
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Access the application at `http://localhost:3000`

## Development

### Frontend Structure

- `src/app/*` - App Router pages and layouts
- `src/components/*` - React components
- `src/lib/*` - Utility functions
- `src/types/*` - TypeScript type definitions

### Backend Structure

- `src/api/*` - API endpoints and controllers
- `src/components/*` - Strapi components
- `src/content-types/*` - Content type definitions

## Deployment

### Frontend

1. Build the application:

   ```bash
   cd frontend
   npm run build
   ```

2. Deploy to your preferred hosting platform (Vercel recommended)

### Backend

1. Build the Strapi application:

   ```bash
   cd backend
   npm run build
   ```

2. Deploy to your preferred hosting platform

## Environment Variables

### Frontend (.env.local)

- `NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY`: Your Stripe publishable key
- `STRIPE_SECRET_KEY`: Your Stripe secret key
- `NEXTAUTH_URL`: The URL of your frontend application
- `NEXTAUTH_SECRET`: A random string for NextAuth session encryption
- `STRAPI_API_URL`: The URL of your Strapi backend

### Backend (.env)

- `APP_KEYS`: Comma-separated list of app keys
- `API_TOKEN_SALT`: Salt for API token generation
- `ADMIN_JWT_SECRET`: Secret for admin JWT tokens
- `JWT_SECRET`: Secret for user JWT tokens
- `STRIPE_SECRET_KEY`: Your Stripe secret key

## Contributing

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

## License

MIT
