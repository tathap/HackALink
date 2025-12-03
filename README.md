# HackaLink - Hackathon Networking Assistant

**People go to hackathons for networking**

[Abhiram Segu](https://github.com/Nightwolf7570/HackALink)
 and I wanted to help people make the most of hackathons and other tech events by helping users supercharge their networking and acquire that one personal connection that can lead to a future job or a new startup. HackALink is the tool for anyone interested in that potential opportunity. We've developed a powerful AI-driven application that aims to help you maximize that hackathon networking experience. We do this in 3 ways: analyzing participant data (given a participant list) on their social media such as LinkedIn and X in order to identify the most influential and accomplished people in various industries to connect with, providing personalized openers and conversation starters based on topics/interests that you might share with these individuals, and helping you generate LinkedIn posts with references to other significant contacts to document your wins and connections to other competitors!

![Next.js](https://img.shields.io/badge/Next.js-14-black)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.3-38B2AC)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--4o-412991)

## Features

### Heavy Hitters Detection
Identify the most influential participants ranked based on their professional background, company prestige, and career achievements across various industries.

### Personalized Talking Points
Get powerful and effective conversation starters tailored to each person's background, interests, and experience. This information is found through scraping publicly available information through Google searches on social media such as LinkedIn and X.

### Team Builder
Find complementary teammates with matching skills and diverse experiences to optimize for the perfect hackathon team and win that prize!

### LinkedIn Post Generator
Create professional posts about your hackathon experience to share wit and grow your network.

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn
- OpenAI API key
- SerpAPI key (for LinkedIn profile discovery)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/hackalink.git
cd hackalink
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env.local
```

Edit `.env.local` with your API keys:

See [SETUP.md](https://github.com/pandeytatha/HackALink/blob/main/SETUP.md)
 for how to get these API keys
```env
# OpenAI
OPENAI_API_KEY=your_openai_api_key

# SerpAPI (for LinkedIn profile discovery)
SERPAPI_API_KEY=your_serpapi_api_key

# Stack Auth 
NEXT_PUBLIC_STACK_PROJECT_ID=your_project_id
NEXT_PUBLIC_STACK_PUBLISHABLE_CLIENT_KEY=your_client_key
STACK_SECRET_SERVER_KEY=your_server_key
```

4. Run the development server:
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Project Structure

```
src/
├── app/                    # Next.js App Router pages
│   ├── api/               # API routes
│   │   ├── participants/  # Participant analysis endpoint
│   │   └── linkedin-post/ # Post generation endpoint
│   ├── dashboard/         # Main analysis dashboard
│   ├── participants/      # Participant list view
│   ├── teams/            # Team builder page
│   └── post/             # LinkedIn post generator
├── components/
│   ├── analysis/         # Analysis result components
│   ├── layout/           # Layout components (Sidebar, PageHeader)
│   ├── participants/     # Participant-related components
│   ├── linkedin/         # LinkedIn post components
│   └── ui/               # Reusable UI components
├── lib/
│   ├── llm-client.ts     # OpenAI integration
│   ├── linkedin-scraper-legal.ts  # SerpAPI integration
│   ├── rate-limiter.ts   # API rate limiting
│   └── services/         # Business logic services
└── types/                # TypeScript type definitions
```

## Legal & Privacy

We do not illegally webscrape from LinkedIn:
- **SerpAPI**: SerpAPI searches Google for publicly available LinkedIn profile information
- **Manual Input**: Users also have the choice to provide direct LinkedIn urls

No direct scraping of LinkedIn is performed.

## License

MIT License - feel free to use this project as a base for your own projects/work!

## Acknowledgments

- Powered by OpenAI GPT-4o API calls
- SerpAPI poweres information aquisition from LinkedIn and other socials
- Thanks to StackAuth for hosting a fire hackathon
