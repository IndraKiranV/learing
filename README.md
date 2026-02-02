# Insha treats - Premium E-commerce Platform

A modern, full-stack e-commerce application for a boutique cake and dessert shop. Built with Next.js 16, TypeScript, and Stripe, featuring a premium design and seamless shopping experience.

## 🚀 Tech Stack

- **Framework:** [Next.js 16](https://nextjs.org/) (App Router)
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Styling:** [Tailwind CSS 4](https://tailwindcss.com/)
- **Database:** [PostgreSQL](https://www.postgresql.org/) with [Prisma ORM](https://www.prisma.io/)
- **Authentication:** [NextAuth.js](https://next-auth.js.org/)
- **Payments:** [Stripe](https://stripe.com/)
- **Testing:** [Jest](https://jestjs.io/) (Unit) & [Playwright](https://playwright.dev/) (E2E)
- **Containerization:** [Docker](https://www.docker.com/)

## 🛠️ Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v20 or higher)
- [npm](https://www.npmjs.com/) (usually comes with Node.js)
- [Docker](https://www.docker.com/) (for running the local database)

## 🏁 Getting Started

1.  **Clone the repository**
    ```bash
    git clone <repository-url>
    cd cakeshop
    ```

2.  **Install dependencies**
    ```bash
    npm install
    ```

3.  **Environment Setup**
    Create a `.env` file in the root directory. You can start by copying the example (if available) or adding the following:
    ```env
    DATABASE_URL="postgresql://postgres:password@localhost:5432/cakeshop"
    NEXTAUTH_SECRET="your-super-secret-key"
    NEXTAUTH_URL="http://localhost:4000"
    
    # Stripe (Test Mode)
    STRIPE_SECRET_KEY="sk_test_..."
    STRIPE_WEBHOOK_SECRET="whsec_..."
    NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY="pk_test_..."
    ```

4.  **Start the Database**
    Use Docker to spin up a PostgreSQL instance:
    ```bash
    # Assuming you have a docker-compose.yml or just run a postgres container
    docker run --name cakeshop-db -e POSTGRES_PASSWORD=password -e POSTGRES_DB=cakeshop -p 5432:5432 -d postgres:15
    ```

5.  **Database Migration & Seeding**
    Initialize the database schema and populate it with sample data:
    ```bash
    npx prisma migrate dev --name init
    npx prisma db seed
    ```

## 🏃‍♂️ Running the Application

Start the development server:

```bash
npm run dev
```

> [!NOTE]
> The application is configured to run on **Port 4000**.
> Open [http://localhost:4000](http://localhost:4000) in your browser.

## 🧪 Running Tests

### Unit Tests
Run the Jest unit test suite:
```bash
npm test
```

### End-to-End (E2E) Tests
Run the Playwright E2E tests:
```bash
npx playwright test
```

## ✨ Features

- **Storefront:** Browse products by category (Cakes, Cupcakes, Cookies, Desserts).
- **Product Details:** View high-quality images, descriptions, and pricing.
- **Shopping Cart:** Add items, adjust quantities, and view total.
- **Checkout:** Secure payment processing via Stripe.
- **Admin Dashboard:** Manage products and view orders (accessible at `/admin`).
- **Responsive Design:** Optimized for mobile, tablet, and desktop.

## 📂 Project Structure

- `src/app`: Next.js App Router pages and layouts.
- `src/components`: Reusable UI components (Header, Footer, etc.).
- `src/lib`: Utility functions and configurations (Stripe, Prisma).
- `prisma`: Database schema and seed scripts.
- `e2e`: Playwright end-to-end tests.

  ## ✨ Features

- **Storefront:** Browse products by category (Cakes, Cupcakes, Cookies, Desserts).
- **Product Details:** View high-quality images, descriptions, and pricing.
- **Shopping Cart:** Add items, adjust quantities, and view total.
- **Checkout:** Secure payment processing via Stripe.
- **Admin Dashboard:** Manage products and view orders (accessible at `/admin`).
- **Responsive Design:** Optimized for mobile, tablet, and desktop.

## 📂 Project Structure

- `src/app`: Next.js App Router pages and layouts.
- `src/components`: Reusable UI components (Header, Footer, etc.).
- `src/lib`: Utility functions and configurations (Stripe, Prisma).
- `prisma`: Database schema and seed scripts.
- `e2e`: Playwright end-to-end tests.

## ✨ Features

- **Storefront:** Browse products by category (Cakes, Cupcakes, Cookies, Desserts).
- **Product Details:** View high-quality images, descriptions, and pricing.
- **Shopping Cart:** Add items, adjust quantities, and view total.
- **Checkout:** Secure payment processing via Stripe.
- **Admin Dashboard:** Manage products and view orders (accessible at `/admin`).
- **Responsive Design:** Optimized for mobile, tablet, and desktop.

## 📂 Project Structure

- `src/app`: Next.js App Router pages and layouts.
- `src/components`: Reusable UI components (Header, Footer, etc.).
- `src/lib`: Utility functions and configurations (Stripe, Prisma).
- `prisma`: Database schema and seed scripts.
- `e2e`: Playwright end-to-end tests.
