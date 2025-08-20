import { Card, CardContent } from "@/components/ui/card"
import { Button } from "@/components/ui/button"
import { motion } from "framer-motion"
import { CheckCircle } from "lucide-react"

export default function PaginaVendaCurso() {
  return (
    <div className="min-h-screen bg-gradient-to-b from-blue-50 to-white text-gray-800">
      {/* Hero Section */}
      <section className="text-center py-20 px-4 max-w-3xl mx-auto">
        <motion.h1
          className="text-4xl md:text-5xl font-bold text-blue-900 mb-4"
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
        >
          Mini Curso sobre Ansiedade
        </motion.h1>
        <p className="text-lg md:text-xl text-gray-600 mb-6">
          Descubra como compreender e lidar com a ansiedade através de um curso prático com técnicas simples, PDFs interativos e um roteiro exclusivo.
        </p>
        <a href="https://pay.kiwify.com.br/SEU-LINK-AQUI" target="_blank" rel="noopener noreferrer">
          <Button size="lg" className="rounded-2xl px-8 py-6 text-lg shadow-md">
            Quero me inscrever agora
          </Button>
        </a>
      </section>

      {/* O que você vai aprender */}
      <section className="max-w-4xl mx-auto px-4 py-12">
        <h2 className="text-2xl font-semibold text-blue-800 mb-6 text-center">O que você vai aprender</h2>
        <div className="grid md:grid-cols-2 gap-6">
          {["O que é ansiedade", "Como funciona no corpo", "Estratégias práticas de controle", "Checklist de autocuidado", "Exercícios de respiração e escrita reflexiva", "Quando buscar ajuda profissional"].map((item, i) => (
            <div key={i} className="flex items-start space-x-3">
              <CheckCircle className="text-green-600 mt-1" />
              <p>{item}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Benefícios */}
      <section className="bg-blue-50 py-12 px-4">
        <h2 className="text-2xl font-semibold text-blue-800 mb-6 text-center">Benefícios do curso</h2>
        <div className="grid md:grid-cols-2 gap-6 max-w-4xl mx-auto">
          {["Reduza sintomas de ansiedade no dia a dia", "Tenha ferramentas práticas para lidar com crises", "Desenvolva hábitos saudáveis de autocuidado", "Acesse material pronto sempre que precisar"].map((benefit, i) => (
            <Card key={i} className="shadow-md rounded-2xl">
              <CardContent className="p-6 text-center text-gray-700">{benefit}</CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* O que você recebe */}
      <section className="max-w-4xl mx-auto px-4 py-12 text-center">
        <h2 className="text-2xl font-semibold text-blue-800 mb-6">O que você recebe</h2>
        <ul className="space-y-3 text-lg">
          <li>📘 PDF Interativo do Mini Curso</li>
          <li>🎤 Roteiro de fala exclusivo</li>
          <li>✅ Checklist de autocuidado</li>
          <li>✍️ Exercícios de escrita reflexiva</li>
        </ul>
      </section>

      {/* CTA final */}
      <section className="text-center py-16 bg-gradient-to-b from-white to-blue-50">
        <h2 className="text-3xl font-bold text-blue-900 mb-6">Pronto para transformar sua relação com a ansiedade?</h2>
        <a href="https://pay.kiwify.com.br/SEU-LINK-AQUI" target="_blank" rel="noopener noreferrer">
          <Button size="lg" className="rounded-2xl px-8 py-6 text-lg shadow-lg">
            Quero meu acesso agora
          </Button>
        </a>
      </section>

      {/* Rodapé */}
      <footer className="bg-blue-900 text-white text-center py-6 mt-12">
        <p>© 2025 Mini Curso Ansiedade. Todos os direitos reservados.</p>
        <p className="text-sm mt-2">Este curso não substitui acompanhamento médico ou psicológico.</p>
      </footer>
    </div>
  )
}
