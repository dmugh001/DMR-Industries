# DMR-Industries
DMR Industries Website
// DMRIndustries.jsx
// Tech-futuristic single-file React component built with Tailwind CSS + Framer Motion.
// Default export: <DMRIndustries />
// How to use:
// 1. Create a React app (Vite or Create React App).
// 2. Install dependencies: framer-motion, lucide-react (icons), and Tailwind CSS configured.
//    npm install framer-motion lucide-react
// 3. Ensure Tailwind is configured for your project.
// 4. Place this file in src/ and import it in your app entry (e.g. index.jsx -> <DMRIndustries />).

import React from 'react';
import { motion } from 'framer-motion';
import { Airplay, Cpu, Zap, Mail, Phone } from 'lucide-react';

const services = [
  {
    id: 1,
    title: 'AI Automation',
    desc: 'Automate repetitive tasks and workflows so your team focuses on high-value work.',
    icon: <Zap className="w-6 h-6" />,
  },
  {
    id: 2,
    title: 'Conversational AI',
    desc: 'Customer support chatbots, lead qualification assistants, and internal knowledge agents.',
    icon: <Airplay className="w-6 h-6" />,
  },
  {
    id: 3,
    title: 'Analytics & Insights',
    desc: 'Turn data into decisions with dashboards, forecasting, and anomaly alerts.',
    icon: <Cpu className="w-6 h-6" />,
  },
];

export default function DMRIndustries() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-black via-slate-900 to-[#030316] text-slate-100 antialiased">
      {/* Navbar */}
      <nav className="max-w-7xl mx-auto px-6 py-6 flex items-center justify-between">
        <div className="flex items-center gap-3">
          <div className="w-12 h-12 bg-gradient-to-br from-[#00ffd5] to-[#0066ff] rounded-xl shadow-lg flex items-center justify-center">
            <span className="font-bold text-black">DMR</span>
          </div>
          <div>
            <div className="font-semibold tracking-wide">DMR Industries</div>
            <div className="text-xs text-slate-400 -mt-0.5">AI Integration for Small Business</div>
          </div>
        </div>
        <div className="hidden md:flex items-center gap-6 text-slate-300">
          <a href="#services" className="hover:text-white">Services</a>
          <a href="#case-studies" className="hover:text-white">Case Studies</a>
          <a href="#contact" className="hover:text-white">Contact</a>
          <button className="ml-4 px-4 py-2 rounded-lg bg-gradient-to-r from-[#00ffd5] to-[#0066ff] text-black font-semibold shadow-md">Get a Quote</button>
        </div>
        <div className="md:hidden">
          <button className="px-3 py-2 rounded bg-slate-800/40">Menu</button>
        </div>
      </nav>

      {/* Hero */}
      <header className="max-w-7xl mx-auto px-6 pt-12 pb-20 flex flex-col md:flex-row items-start gap-10">
        <div className="flex-1">
          <motion.h1
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ delay: 0.1 }}
            className="text-4xl md:text-6xl font-extrabold leading-tight"
          >
            Deploy AI. Drive Growth.
            <span className="block text-transparent bg-clip-text bg-gradient-to-r from-[#00ffd5] to-[#7b61ff]">for small business.</span>
          </motion.h1>

          <motion.p
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ delay: 0.25 }}
            className="mt-6 text-slate-300 max-w-xl"
          >
            DMR Industries helps small businesses adopt practical, measurable AI solutions — from chatbots that convert leads to automations that save hours every week.
          </motion.p>

          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ delay: 0.4 }}
            className="mt-8 flex gap-4"
          >
            <a href="#contact" className="px-6 py-3 rounded-lg bg-gradient-to-r from-[#00ffd5] to-[#0066ff] text-black font-semibold shadow-lg">Start a Project</a>
            <a href="#services" className="px-6 py-3 rounded-lg border border-slate-700 text-slate-200">See Services</a>
          </motion.div>

          <motion.div
            className="mt-10 text-slate-400 text-sm"
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ delay: 0.6 }}
          >
            <strong>Quick wins:</strong> AI-powered appointment reminders, automatic invoice categorization, and sales lead triage — delivered in 4–8 weeks.
          </motion.div>
        </div>

        {/* Right visual / demo panel */}
        <motion.div
          initial={{ opacity: 0, scale: 0.98 }}
          animate={{ opacity: 1, scale: 1 }}
          transition={{ delay: 0.35 }}
          className="w-full md:w-1/2 lg:w-2/5"
        >
          <div className="rounded-2xl p-6 bg-gradient-to-br from-[#041024]/60 to-[#071029]/40 border border-slate-800 shadow-2xl">
            <div className="flex items-center justify-between">
              <div>
                <div className="text-sm text-slate-400">Live Demo</div>
                <div className="text-lg font-semibold">AI Sales Assistant</div>
              </div>
              <div className="text-xs text-slate-500">Prototype</div>
            </div>

            <div className="mt-6 bg-slate-900/40 rounded-xl p-4 min-h-[220px]">
              <div className="text-slate-300 mb-3">Ask the assistant a question:</div>
              <div className="flex gap-2">
                <input className="flex-1 bg-transparent border border-slate-800 rounded-lg px-3 py-2 text-slate-200 placeholder-slate-500" placeholder="How many new leads this month?" />
                <button className="px-4 py-2 rounded-lg bg-gradient-to-r from-[#00ffd5] to-[#0066ff] text-black font-semibold">Ask</button>
              </div>

              <div className="mt-4 text-slate-400 text-sm">Response</div>
              <div className="mt-2 bg-[#0b1220] rounded-md p-3 text-slate-200 text-sm">The assistant can summarize lead sources, predict close probability, and recommend next outreach steps.</div>
            </div>

            <div className="mt-4 flex items-center justify-between text-xs text-slate-500">
              <div>Secure • Compliant • On-prem or Cloud</div>
              <div className="flex items-center gap-2">
                <div className="w-2 h-2 bg-[#00ffbf] rounded-full" /> <span>Realtime</span>
              </div>
            </div>
          </div>
        </motion.div>
      </header>

      {/* Services */}
      <section id="services" className="max-w-7xl mx-auto px-6 py-16">
        <motion.div
          initial={{ opacity: 0, y: 10 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ delay: 0.1 }}
          className="grid md:grid-cols-3 gap-8"
        >
          {services.map((s) => (
            <div key={s.id} className="rounded-xl p-6 bg-gradient-to-br from-[#051027] to-[#07102a] border border-slate-800/60 shadow-md">
              <div className="flex items-center gap-4">
                <div className="p-3 rounded-lg bg-slate-800/40">{s.icon}</div>
                <div>
                  <div className="font-semibold">{s.title}</div>
                  <div className="text-sm text-slate-400">{s.desc}</div>
                </div>
              </div>

              <div className="mt-6 flex items-center gap-3">
                <a className="text-sm text-slate-300 hover:text-white">Learn more →</a>
                <div className="ml-auto text-xs text-slate-500">Turnkey • Secure</div>
              </div>
            </div>
          ))}
        </motion.div>
      </section>

      {/* Case Studies */}
      <section id="case-studies" className="max-w-7xl mx-auto px-6 py-8">
        <motion.h2 initial={{ opacity: 0 }} animate={{ opacity: 1 }} className="text-2xl font-bold">Case Studies & Results</motion.h2>
        <div className="mt-6 grid md:grid-cols-3 gap-6">
          <article className="p-5 rounded-xl bg-gradient-to-br from-[#021021] to-[#041029] border border-slate-800/40">
            <div className="text-slate-400 text-sm">Retail</div>
            <div className="mt-2 font-semibold">Inventory automation</div>
            <div className="mt-3 text-slate-300 text-sm">Reduced stockouts by 42% and freed 10 weekly hours for the store manager.</div>
          </article>

          <article className="p-5 rounded-xl bg-gradient-to-br from-[#021021] to-[#041029] border border-slate-800/40">
            <div className="text-slate-400 text-sm">Services</div>
            <div className="mt-2 font-semibold">AI triage for leads</div>
            <div className="mt-3 text-slate-300 text-sm">Increased qualified leads by 28% and shortened response times.</div>
          </article>

          <article className="p-5 rounded-xl bg-gradient-to-br from-[#021021] to-[#041029] border border-slate-800/40">
            <div className="text-slate-400 text-sm">Healthcare (SMB clinic)</div>
            <div className="mt-2 font-semibold">Appointment automation</div>
            <div className="mt-3 text-slate-300 text-sm">No-show rates dropped 15% after intelligent reminders and rescheduling flows.</div>
          </article>
        </div>
      </section>

      {/* Process / How we work */}
      <section className="max-w-7xl mx-auto px-6 py-12">
        <div className="bg-gradient-to-br from-[#041024]/40 to-[#071029]/30 rounded-xl p-8 border border-slate-800">
          <div className="md:flex md:items-center md:justify-between">
            <div>
              <h3 className="text-xl font-bold">Our process</h3>
              <p className="text-slate-400 mt-2">Fast discovery, prioritized roadmap, pilot deployment, and scale — all transparent and outcome-driven.</p>
            </div>
            <div className="mt-6 md:mt-0 flex gap-4">
              <div className="p-4 rounded-lg bg-slate-900/40 text-center">
                <div className="font-semibold">1. Discover</div>
                <div className="text-sm text-slate-400 mt-1">Identify highest-impact opportunities.</div>
              </div>
              <div className="p-4 rounded-lg bg-slate-900/40 text-center">
                <div className="font-semibold">2. Pilot</div>
                <div className="text-sm text-slate-400 mt-1">Prove value with measurable KPIs.</div>
              </div>
              <div className="p-4 rounded-lg bg-slate-900/40 text-center">
                <div className="font-semibold">3. Scale</div>
                <div className="text-sm text-slate-400 mt-1">Operationalize and iterate.</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="max-w-7xl mx-auto px-6 py-16">
        <div className="grid md:grid-cols-2 gap-8">
          <div className="rounded-xl p-8 bg-gradient-to-br from-[#041024] to-[#071029] border border-slate-800/40">
            <h3 className="text-2xl font-bold">Start your AI project</h3>
            <p className="text-slate-400 mt-2">Tell us about your business and we’ll propose a high-impact pilot.</p>

            <form className="mt-6 grid gap-3">
              <input className="bg-transparent border border-slate-800 rounded-md px-3 py-2 text-slate-200" placeholder="Full name" />
              <input className="bg-transparent border border-slate-800 rounded-md px-3 py-2 text-slate-200" placeholder="Business email" />
              <input className="bg-transparent border border-slate-800 rounded-md px-3 py-2 text-slate-200" placeholder="Company (optional)" />
              <select className="bg-transparent border border-slate-800 rounded-md px-3 py-2 text-slate-200">
                <option className="bg-[#041022]">What are you interested in?</option>
                <option>Automation</option>
                <option>Chatbot</option>
                <option>Analytics</option>
              </select>
              <textarea className="bg-transparent border border-slate-800 rounded-md px-3 py-2 text-slate-200" placeholder="Describe your challenge (1-2 sentences)" rows={4} />

              <div className="flex items-center gap-3 mt-2">
                <button type="button" className="px-5 py-3 rounded-lg bg-gradient-to-r from-[#00ffd5] to-[#0066ff] text-black font-semibold">Request Proposal</button>
                <button type="button" className="px-5 py-3 rounded-lg border border-slate-700 text-slate-300">Schedule Call</button>
              </div>
            </form>

            <div className="mt-6 text-slate-400 text-sm flex items-center gap-4">
              <Mail className="w-4 h-4" /> <div>hello@dmr.industries</div>
            </div>
          </div>

          <div className="rounded-xl p-8 bg-gradient-to-br from-[#021020] to-[#041021] border border-slate-800/40">
            <h4 className="font-semibold">Why small businesses choose DMR</h4>
            <ul className="mt-4 space-y-3 text-slate-300 text-sm">
              <li>• Rapid pilot delivery (4–8 weeks)</li>
              <li>• No heavy upfront engineering fees</li>
              <li>• Clear ROI metrics and handover docs</li>
              <li>• Flexible hosting: cloud, hybrid, or on-prem</li>
            </ul>

            <div className="mt-6">
              <div className="text-slate-400 text-sm">Phone</div>
              <div className="font-medium">(555) 555-0123</div>
            </div>

            <div className="mt-6">
              <div className="text-slate-400 text-sm">Address</div>
              <div className="font-medium">Remote / NYC</div>
            </div>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="border-t border-slate-800/40 mt-12">
        <div className="max-w-7xl mx-auto px-6 py-8 flex flex-col md:flex-row items-center justify-between gap-4">
          <div className="text-sm text-slate-400">© {new Date().getFullYear()} DMR Industries — AI integration for small business</div>
          <div className="flex items-center gap-6 text-slate-300">
            <a className="hover:text-white">Privacy</a>
            <a className="hover:text-white">Terms</a>
            <a className="hover:text-white flex items-center gap-2"><Phone className="w-4 h-4" /> Contact</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
