# DemersonCassiano.github.io
Meu web site
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

const works = [
  {
    title: "Ilustração 3D para Interiores",
    description: "Projetos detalhados de ambientes internos em parceria com marcenarias, focando em móveis sob medida e soluções personalizadas.",
    image: "/images/interiores.jpg"
  },
  {
    title: "Fachadas Comerciais",
    description: "Desenvolvimento de fachadas em colaboração com empresas de comunicação visual, incluindo estrutura, ACM e fixação.",
    image: "/images/fachadas.jpg"
  },
  {
    title: "Renderização para Arquitetos",
    description: "Terceirização de renderizações hiper-realistas para arquitetos que precisam otimizar o tempo de projeto.",
    image: "/images/renderizacao.jpg"
  },
  {
    title: "PCP para Marcenarias",
    description: "Desenvolvimento de descritivos e quantitativos completos de materiais como MDF, ferragens e acessórios para montagem de móveis.",
    image: "/images/pcp.jpg"
  },
  {
    title: "Descritivos de Montagem em Comunicação Visual",
    description: "Detalhamento técnico para montagem de fachadas com estruturas metálicas, ACM e elementos de fixação.",
    image: "/images/montagem.jpg"
  },
];

export default function Portfolio() {
  return (
    <div className="p-6 max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div className="md:col-span-2 lg:col-span-3 text-center">
        <h1 className="text-4xl font-bold mb-2">3D.On, Projetos, Ilustrações 3D e PCP</h1>
        <p className="text-lg text-gray-600 max-w-2xl mx-auto">Portfólio de desenvolvimento e renderização de projetos 3D para interiores, fachadas e marcenarias, com foco em qualidade e detalhamento técnico.</p>
      </div>
      {works.map((work, idx) => (
        <motion.div key={idx} whileHover={{ scale: 1.03 }}>
          <Card className="rounded-2xl shadow-md overflow-hidden">
            <img src={work.image} alt={work.title} className="w-full h-48 object-cover" />
            <CardContent className="p-4">
              <h2 className="text-xl font-semibold mb-2">{work.title}</h2>
              <p className="text-gray-700 text-base">{work.description}</p>
            </CardContent>
          </Card>
        </motion.div>
      ))}
      <div className="md:col-span-2 lg:col-span-3 text-center mt-6">
        <Button className="text-lg px-6 py-2 rounded-2xl">Entre em Contato</Button>
        <p className="text-sm text-gray-500 mt-4">© {new Date().getFullYear()} 3D.On, Projetos, Ilustrações 3D e PCP. Todos os direitos reservados.</p>
      </div>
    </div>
  );
}
