# IndCourtOrder AI ⚖️

> **Disclaimer**: This website generates fictional legal documents for demonstration purposes only. It is not related to any real court or judge. It is built strictly for fun and educational purposes (to jokingly "make fear among the wrongdoers"). Do not use it for actual legal or fraudulent purposes.

An AI-powered Next.js application that generates realistic, judicial-style legal notices. By leveraging Google's Gemini 1.5 Pro via the Genkit framework, the app produces highly formal, authoritative court orders complete with corresponding Indian Penal Code (IPC) sections based on user-provided grievances.

## 🌟 Features

- **AI-Powered Legal Notices**: Uses Google Gemini 1.5 Pro to generate cold, harsh, and formal legal texts.
- **IPC Section Suggestions**: Automatically identifies and lists relevant Indian Penal Code sections based on the described incident.
- **PDF Export**: Generate and download the court orders as professionally formatted PDF files (powered by `jspdf` and `html2canvas`).
- **Modern UI**: Built with Next.js App Router, Tailwind CSS, and shadcn/ui components for a sleek and responsive user experience.

## 🛠️ Tech Stack

- **Framework**: [Next.js 15](https://nextjs.org/) (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS & [shadcn/ui](https://ui.shadcn.com/)
- **AI Integration**: Google GenAI (Gemini 1.5 Pro) via [Genkit](https://firebase.google.com/docs/genkit)
- **Forms & Validation**: React Hook Form + Zod
- **PDF Generation**: `jspdf` & `html2canvas`

## 📁 Project Structure

```text
src/
├── ai/          # Genkit configuration and AI flows (generate-court-order.ts)
├── app/         # Next.js App Router pages and layouts
├── components/  # Reusable UI components (shadcn/ui) and form logic
├── hooks/       # Custom React hooks
└── lib/         # Utility functions (shadcn/ui utils, etc.)
```

## 🚀 Setup Instructions

### Local Development

1. **Clone the repository and install dependencies:**
   ```bash
   npm install
   ```

2. **Configure Environment Variables:**
   Create a `.env.local` file in the root directory and add your Gemini API key:
   ```env
   GEMINI_API_KEY=your_actual_api_key_here
   ```
   *(Note: You can also use `GOOGLE_GENAI_API_KEY` or `GOOGLE_API_KEY`)*

3. **Run the development server:**
   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

### Vercel Deployment

If you are deploying this project on Vercel, you need to add the API key to your Vercel project settings:

1. Go to your Vercel Project > **Settings** > **Environment Variables**.
2. Add a new variable with the key `GEMINI_API_KEY` and your actual API key as the value.
3. **Important:** Ensure you trigger a **Redeploy** (Deployments > three dots > Redeploy) after adding or changing the environment variable so it gets included in the build.
