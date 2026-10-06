# Notion-Style Productivity Workspace

A full-stack, real-time productivity application built to replicate the core experience of Notion. This workspace provides a flexible and intuitive platform for users to create, organize, and seamlessly manage their notes and files.

## ✨ Features

### Productivity & Organization
* **Notion-Style Editor:** A highly responsive rich-text editor for seamless note-taking.
* **Hierarchical Documents:** Infinite children documents for deep, structured organization.
* **Intuitive Management:** Drag-and-drop functionality for easy file reordering.
* **Navigation Sidebar:** Fully expandable and collapsible sidebar with quick-access pinned documents.
* **Trash & Recovery:** Soft delete functionality with options to permanently delete or restore files.

### User Experience
* **Customization:** Add cover images and customizable icons (with real-time updates) to personalize your workspace.
* **Theming:** Built-in Light and Dark modes.
* **Responsive Design:** Fully optimized for mobile and desktop productivity on the go.
* **Landing Page:** A welcoming and modern entry point for new users.

### Data, Security & Sharing
* **Real-Time Sync:** Instant data updates across all active sessions.
* **File Management:** Upload, delete, and replace images/files directly within documents.
* **Authentication:** Secure user login and session management.
* **Web Publishing:** Generate public links to share specific notes with the world.

## 🛠️️ Technologies
* **Frontend:** React, Next.js
* **Database:** [Convex](https://www.convex.dev/) (Real-time database and backend logic)
* **File Storage:** [EdgeStore](https://edgestore.dev/) (Distributed key-value store for image/file uploads)
* **Authentication:** [Clerk](https://clerk.com/) (Secure and scalable user auth)

## 🚀 Getting Started

*Note: This demo currently runs on Clerk development keys, so standard user limits apply. For long-term use, you will need to set up your own production keys.*

### 1. Clone the repository
```bash
git clone <your-repo-url>
cd <your-repo-directory>
```

### 2. Install dependencies
```bash
npm install
```

### 3. Set up environment variables
Copy the `.env.example` file to a new `.env.local` file:
```bash
cp .env.example .env.local
```
Populate the file with your API keys from Convex, Clerk, and EdgeStore:
```env
# From Convex dashboard
CONVEX_DEPLOYMENT=
NEXT_PUBLIC_CONVEX_URL=

# From Clerk dashboard
CLERK_JWT_ISSUER_DOMAIN=
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

# From EdgeStore dashboard
EDGE_STORE_ACCESS_KEY=
EDGE_STORE_SECRET_KEY=
```

### 4. Run Convex (Backend)
Initialize and run the Convex development environment:
```bash
npx convex dev
```

### 5. Start the Development Server
In a new terminal window, start the frontend application:
```bash
npm run dev
```
