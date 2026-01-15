# 🔥 Cinder - Real-time Ephemeral Chat

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

> **Secure, instant, voicemail-style text conversations that leave no trace.**  
> Cinder allows you to create temporary chat rooms, share a link, and communicate in real-time. Once the room is destroyed or the timer runs out, everything is gone forever.

---

## 🚀 Features

- **⚡ Real-time Messaging**: Instant message delivery using WebSocket/Server-Sent Events via Upstash Realtime.
- **⏳ Ephemeral Rooms**: Rooms have a Time-to-Live (TTL) and automatically self-destruct.
- **🔒 Privacy First**: No persistent history beyond the room's lifespan.
- **💅 Modern UI**: Built with a sleek, dark-themed responsive design using Tailwind CSS.
- **🔗 Instant Sharing**: Create a room with one click and share the link instantly.
- **☢️ Manual Self-Destruct**: Room creators can nuke the room at any time.

---

## 🛠️ Tech Stack

This project is built with a cutting-edge stack focused on speed and simplicity:

| Category | Technology | Description |
|----------|------------|-------------|
| **Framework** | [![Next.js](https://img.shields.io/badge/Next.js-16-black?style=flat&logo=next.js)](https://nextjs.org/) | React Framework for Production (App Router) |
| **Backend API** | [![ElysiaJS](https://img.shields.io/badge/ElysiaJS-Fast-blueviolet?style=flat)](https://elysiajs.com/) | Ergonomic Framework for TypeScript |
| **Database** | [![Upstash Redis](https://img.shields.io/badge/Upstash-Redis-00E9A3?style=flat&logo=redis)](https://upstash.com/) | Serverless Redis for data persistence |
| **Realtime** | [![Upstash Realtime](https://img.shields.io/badge/Upstash-Realtime-00E9A3?style=flat&logo=redis)](https://upstash.com/docs/realtime) | Pub/Sub for live chat updates |
| **Styling** | [![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=flat&logo=tailwind-css)](https://tailwindcss.com/) | Utility-first CSS framework |
| **State/Query** | [![TanStack Query](https://img.shields.io/badge/TanStack-Query-FF4154?style=flat)](https://tanstack.com/query) | Async state management |
| **Validation** | [![Zod](https://img.shields.io/badge/Zod-Validation-3068b7?style=flat)](https://zod.dev/) | TypeScript-first schema validation |

---

## 📂 Project Structure

```bash
📦 realtime_chat
├── 📂 src
│   ├── 📂 app              # Next.js App Router pages
│   │   ├── 📂 api          # ElysiaJS API routes
│   │   ├── 📂 room         # Room pages ([roomId])
│   │   └── page.tsx        # Landing/Lobby page
│   ├── 📂 components       # React components
│   ├── 📂 hooks            # Custom hooks (useUsername, etc.)
│   └── 📂 lib              # Utilities (Redis, Realtime client)
├── 📄 package.json         # Dependencies and scripts
├── 📄 tailwind.config.ts   # Tailwind configuration
└── 📄 public               # Static assets
```

---

## 🏁 Getting Started

Follow these steps to set up the project locally.

### 1. Prerequisites

- **Node.js** (v18 or higher)
- **npm** or **yarn** or **pnpm**
- An **Upstash** account (for Redis and Realtime)

### 2. Installation

Clone the repository and install dependencies:

```bash
# Clone the repo
git clone https://github.com/MukundhArul/Cinder.git

# Navigate to the directory
cd Cinder

# Install dependencies (using npm 7+ to handle peer deps if needed, or just npm install)
npm install
```

### 3. Environment Configuration

Create a `.env` file in the root directory and add your Upstash credentials:

```bash
# .env
UPSTASH_REDIS_REST_URL="your-upstash-redis-rest-url"
UPSTASH_REDIS_REST_TOKEN="your-upstash-redis-rest-token"
```

> **Note:** You can create a free Redis database at [console.upstash.com](https://console.upstash.com/).

### 4. Running Locally

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 📖 Usage Guide

1.  **Enter a Username**: On the home page, you'll be assigned a random username (or you can set one if implemented).
2.  **Create a Room**: Click "Create Room" to generate a unique, secure chat lobby.
3.  **Share**: Copy the URL and send it to a friend.
4.  **Chat**: Messages appear instantly for all participants.
5.  **Destroy**: 
    - The room has a countdown timer.
    - You can click the "DESTROY NOW" button to wipe the room and all messages immediately.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/MukundhArul">MukundhArul</a> for the Future of Chat.
</p>
