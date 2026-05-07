# 📱 Telkom University LMS - Mobile App

Aplikasi Learning Management System (LMS) untuk mahasiswa Telkom University dengan desain mobile-first menggunakan React, React Router, dan Tailwind CSS.

## ✨ Fitur Utama

- 🏠 **Dashboard Home** - Ringkasan mata kuliah dan tugas
- 📚 **Course Management** - Daftar dan detail mata kuliah dengan progress tracking
- 📖 **Learning Materials** - Sistem pembelajaran berbasis minggu (collapsible)
- ✍️ **Assignment Submission** - Upload tugas dengan preview dan notifikasi
- 🔔 **Notifications** - Sistem notifikasi dengan filter
- 👤 **User Profile** - Informasi mahasiswa lengkap
- ⚙️ **Settings** - Edit profil dan toggle dark mode
- 🔐 **Authentication** - Halaman login dengan validasi form

## 🎨 Design System

- **Primary Color**: Maroon (#800000) - Warna identitas Telkom University
- **Typography**: System font stack
- **Components**: Radix UI + Custom components
- **Dark Mode**: Full support dengan localStorage persistence
- **Responsive**: Mobile-first design (iPhone 11 compatible)

## 🚀 Deploy ke Vercel via GitHub

### Langkah 1: Push ke GitHub

1. Inisialisasi Git repository (jika belum):
\`\`\`bash
git init
git add .
git commit -m "Initial commit: Telkom University LMS App"
\`\`\`

2. Buat repository baru di GitHub

3. Push code ke GitHub:
\`\`\`bash
git remote add origin https://github.com/username/telkom-lms-app.git
git branch -M main
git push -u origin main
\`\`\`

### Langkah 2: Deploy ke Vercel

#### Opsi A: Via Vercel Dashboard (Recommended)

1. Buka [vercel.com](https://vercel.com) dan login
2. Klik **"Add New Project"**
3. Import repository GitHub Anda
4. Vercel akan otomatis detect konfigurasi:
   - **Framework Preset**: Vite
   - **Build Command**: `pnpm run build`
   - **Output Directory**: `dist`
   - **Install Command**: `pnpm install`
5. Klik **"Deploy"**

#### Opsi B: Via Vercel CLI

\`\`\`bash
# Install Vercel CLI
npm i -g vercel

# Login ke Vercel
vercel login

# Deploy
vercel

# Deploy ke production
vercel --prod
\`\`\`

### Langkah 3: Konfigurasi Domain (Opsional)

1. Di Vercel Dashboard, buka project Anda
2. Pergi ke **Settings → Domains**
3. Tambahkan custom domain atau gunakan domain `.vercel.app` gratis

## 🛠️ Development

### Prerequisites

- Node.js 18+ 
- pnpm (recommended) atau npm

### Installation

\`\`\`bash
# Install dependencies
pnpm install

# Jalankan development server
pnpm dev

# Build untuk production
pnpm build

# Preview production build
pnpm preview
\`\`\`

### Environment Variables

Tidak ada environment variables yang diperlukan untuk saat ini. Semua data menggunakan mock data lokal.

## 📦 Tech Stack

- **Framework**: React 18.3.1
- **Routing**: React Router 7.13.0
- **Styling**: Tailwind CSS 4.1.12
- **Build Tool**: Vite 6.3.5
- **UI Components**: Radix UI
- **Icons**: Lucide React
- **Package Manager**: pnpm
- **Deployment**: Vercel

## 📱 Halaman Aplikasi

1. `/login` - Halaman Login
2. `/` - Dashboard Home
3. `/courses` - Daftar Mata Kuliah
4. `/course/:courseId` - Detail Mata Kuliah
5. `/course/:courseId/material/:materialId` - Detail Materi Pembelajaran
6. `/assignment/:assignmentId` - Detail & Submit Tugas
7. `/notifications` - Notifikasi
8. `/profile` - Profil Mahasiswa
9. `/settings` - Pengaturan

## 🔒 Authentication Flow

- Default: User diarahkan ke `/login`
- Setelah login: Redirect ke `/` (Home)
- Protected routes: Semua halaman kecuali `/login`
- Logout: Hapus session dan redirect ke `/login`

## 💾 Data Persistence

- **User Profile**: localStorage (`userData`)
- **Theme**: localStorage (`theme`)
- **Auth Status**: localStorage (`isLoggedIn`)

## 🎯 Fitur Mendatang (Optional)

- [ ] Backend integration dengan REST API
- [ ] Real-time notifications dengan WebSocket
- [ ] File upload ke cloud storage
- [ ] Push notifications
- [ ] Offline mode dengan Service Worker
- [ ] Multi-language support

## 📄 License

Private - Telkom University LMS

## 👨‍💻 Developer

Built with ❤️ for Telkom University students

---

**Ready to deploy!** 🚀
