# Project.Hub
Server developer 
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

export default function ProjectHubSite() {
  return (
    <div
      className="min-h-screen bg-cover bg-center text-white"
      style={{
        backgroundImage: "url('/black-glitter.jpg')",
      }}
    >
      <div className="backdrop-blur-sm bg-black/60 min-h-screen p-6">
        <header className="flex flex-col items-center text-center mb-10">
          <img
            src="/projecthub-logo.png"
            alt="ProjectHub Logo"
            className="w-32 h-32 rounded-2xl shadow-lg mb-4"
          />
          <h1 className="text-4xl font-bold">ProjectHub</h1>
          <p className="text-lg mt-2">Discord Server Developer</p>
        </header>

        <section className="grid md:grid-cols-3 gap-6 mb-10">
          {[
            {
              title: "Welcome & Goodbye System",
              price: "30 RON",
              desc: "Mesaje automate personalizate pentru membri noi și cei care pleacă.",
            },
            {
              title: "Security Setup",
              price: "50 RON",
              desc: "Protecție anti-raid, anti-spam și roluri sigure.",
            },
            {
              title: "Server Backup",
              price: "40 RON",
              desc: "Backup complet pentru server în caz de probleme.",
            },
            {
              title: "Role & Permissions",
              price: "25 RON",
              desc: "Configurare roluri și permisiuni profesionale.",
            },
            {
              title: "Bots Setup",
              price: "35 RON",
              desc: "Instalare și configurare boturi utile.",
            },
            {
              title: "Full Server Setup",
              price: "120 RON",
              desc: "Server complet de la 0 (toate sistemele incluse).",
            },
          ].map((service, index) => (
            <motion.div
              key={index}
              initial={{ opacity: 0, y: 30 }}
              animate={{ opacity: 1, y: 0 }}
              transition={{ delay: index * 0.1 }}
            >
              <Card className="bg-black/70 border-white/10 rounded-2xl shadow-xl">
                <CardContent className="p-4">
                  <h2 className="text-xl font-semibold">{service.title}</h2>
                  <p className="text-sm opacity-80 mt-2">{service.desc}</p>
                  <p className="mt-4 text-lg font-bold">{service.price}</p>
                </CardContent>
              </Card>
            </motion.div>
          ))}
        </section>

        <section className="text-center mb-10">
          <p className="text-lg">📅 Program: Vineri - Duminică</p>
          <p className="text-lg">💳 Plată: Doar Revolut</p>
        </section>

        <div className="flex justify-center">
          <a
            href="https://www.tiktok.com/@negr_thau?_r=1&_t=ZN-95kLLMlYRBW"
            target="_blank"
          >
            <Button className="text-lg px-6 py-3 rounded-2xl shadow-lg">
              Vezi TikTok
            </Button>
          </a>
        </div>
      </div>
    </div>
  );
}
