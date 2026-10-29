<div align="center">

# ⚡ Gerador de Placa Pix Profissional

**Crie e imprima placas Pix personalizadas para o seu estabelecimento em segundos.**  
Formatos prontos para Folha A4 (Parede/Porta) e Totem de Balcão (A5), com temas modernos, inclusão de logotipo da empresa e conformidade oficial com o Banco Central do Brasil (EMVCo).

[![Licença MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![HTML5 / Vanilla CSS](https://img.shields.io/badge/tech-HTML5%20%7C%20CSS3%20%7C%20JavaScript-blue.svg)](#)
[![Banco Central](https://img.shields.io/badge/PIX-Banco%20Central%20do%20Brasil-32BCAD.svg)](#)
[![Print Ready](https://img.shields.io/badge/Print-A4%20%26%20A5-orange.svg)](#)

[![Live Demo](https://img.shields.io/badge/Demo-Acessar%20Online-32BCAD?style=for-the-badge&logo=google-chrome&logoColor=white)](https://rikelmi12.github.io/gerador-placa-pix/)

[🚀 Acessar Demonstração Online](https://rikelmi12.github.io/gerador-placa-pix/) • [Recursos](#-recursos-principais) • [Temas](#-temas-disponíveis) • [Padrão BACEN](#-especificação-técnica-pix)

</div>

---

## 🌟 Recursos Principais

- 🏢 **Identidade da Empresa na Placa**:
  - Nome fantasia e slogan/subtítulo em destaque com tipografia profissional.
  - Upload direto do logotipo da sua empresa (PNG, JPG, SVG, WebP) com exibição automática na folha.
- 🎨 **7 Temas Visuais Exclusivos**:
  - Paletas de cores para diferentes ramos de atividade (Dark & Gold, Turquesa Pix Oficial, Azul Corporativo, Esmeralda Saúde, Roxo Fintech, Vermelho Gourmet e Minimalista P&B).
- 📐 **Formatos para Impressão**:
  - **Folha A4 Completa (210 x 297 mm)**: Perfeita para afixar em paredes, portas, quadros decorativos ou vitrines.
  - **Display / Totem de Balcão (A5)**: Compacto para suportes acrílicos ao lado da máquina de cartão ou no caixa.
- 🖨️ **Impressão Otimizada (@media print)**:
  - Estilização calibrada em milímetros exatos, sem cortes de bordas e sem páginas extras em branco.
- 📱 **QR Code de Alta Definição (300+ DPI)**:
  - Leitura instantânea por qualquer câmera ou aplicativo bancário brasileiro (Nubank, Itaú, Bradesco, Santander, Banco do Brasil, Inter, etc.).
- 📋 **Pix Copia e Cola**:
  - Botão com cópia instantânea do payload oficial para WhatsApp ou mensagens.
- 🖼️ **Exportação como Imagem PNG**:
  - Baixe a placa pronta em imagem de alta resolução.
- 🔒 **100% Client-Side**:
  - Funciona totalmente no navegador, sem salvar suas chaves em servidores externos. Privacidade e segurança totais.

---

## 🎨 Temas Disponíveis

| Tema | Paleta | Indicação de Uso |
| :--- | :--- | :--- |
| **Pix Oficial** | Turquesa (#32BCAD) & Petróleo | Padrão Banco Central universal e confiável |
| **Ouro Nobre** | Preto Fosco & Dourado Real | Barbearias, clínicas de estética, joalherias e alta gastronomia |
| **Corporativo** | Azul Royal (#2563EB) & Slate | Lojas formais, consultórios, escritórios e serviços |
| **Esmeralda** | Verde Jóia (#059669) & Menta | Farmácias, empórios naturais, academias e pet shops |
| **Roxo Fintech** | Roxo Neon (#7C3AED) & Lilás | Moda jovem, tech shops, estúdios criativos e tatuagem |
| **Gourmet** | Vermelho Carmim (#DC2626) & Vinho | Restaurantes, hamburguerias, pizzarias, bares e padarias |
| **Minimalista** | Monocromático Puro Preto & Branco | Cafés artesanais, marcas autorais, arquitetura e boutiques |

---

## 📋 Especificação Técnica (Pix EMVCo)

O gerador segue rigorosamente a especificação técnica dos arranjos de pagamento instantâneo do **Banco Central do Brasil**:

- **ID 00**: Formato de Payload (`01`)
- **ID 26**: Merchant Account Information (`br.gov.bcb.pix` + Chave Pix limpa)
- **ID 52**: Merchant Category Code (`0000`)
- **ID 53**: Código da Moeda (`986` - Real BRL)
- **ID 54**: Valor da Cobrança (Opcional, com 2 casas decimais)
- **ID 58**: Código do País (`BR`)
- **ID 59**: Nome do Recebedor (normalizado sem acentos, até 25 caracteres)
- **ID 60**: Cidade do Recebedor (normalizado sem acentos, até 15 caracteres)
- **ID 62**: Campo Adicional / TxID (`***` ou personalizado)
- **ID 63**: Checksum CRC-16 (Polinômio 0x1021, valor inicial 0xFFFF)

---

## 🚀 Como Usar

### 1. No Navegador Local
Não requer instalação de Node, Python ou servidores. Basta dar **dois cliques** no arquivo `index.html`:

```bash
# Ou clone o repositório:
git clone https://github.com/rikelmi12/gerador-placa-pix.git
cd gerador-placa-pix

# E abra no navegador:
start index.html
```

### 2. No GitHub Pages
Basta acessar as configurações do repositório no GitHub (`Settings > Pages`) e selecionar o branch `main` na raiz (`/`). O gerador estará disponível online imediatamente.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5** Estrutura semântica
- **CSS3 Puro** Variáveis CSS, Glassmorphism, CSS Grid & Flexbox, `@media print`
- **JavaScript (ES6+)** Lógica de cálculo EMVCo e algoritmo CRC16-CCITT
- **[QRCode.js](https://github.com/davidshimjs/qrcodejs)** Renderização vetorial do código QR
- **[html2canvas](https://html2canvas.hertzen.com/)** Exportação de imagem PNG de alta definição
- **Google Fonts** (`Outfit`, `Plus Jakarta Sans`, `JetBrains Mono`)

---

## 📄 Licença

Distribuído sob a licença [MIT](LICENSE). Consulte `LICENSE` para mais detalhes.

---

<div align="center">
Desenvolvido com foco em estética, usabilidade e precisão técnica.
</div>
