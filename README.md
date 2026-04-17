# 🏪 Vitrine Local - Comparador de Ofertas

Um protótipo de alta fidelidade "Search-First" voltado para o comércio local (Farmácias, Padarias e Mercados). O projeto tem como foco principal a comparação rápida de preços de produtos entre diferentes lojistas da região, com uma interface Premium inspirada em gigantes do mercado como iFood, Mercado Livre e Rappi.

O aplicativo foi arquitetado em um **arquivo único (`index.html`)** com dados estruturados (mocado) em formato JSON, permitindo que a validação de Front-End e UX/UI seja feita instantaneamente, necessitando apenas clicar e abrir no navegador, sem precisar instalar Node.js ou rodar servidores locais.

---

## 🚀 Funcionalidades Implementadas

O protótipo já conta com um roteamento em memória de três telas distintas (Single-Page App local):

### 1. Vitrine Comparativa (Home)
- **Busca em Tempo Real**: Barra de pesquisa para encontrar produtos instantaneamente pelo nome.
- **Filtros por Categoria**: Navegação por tipos de comércio específicos (Farmácia, Padaria, Mercado).
- **Ordenação Dinâmica**: Os resultados podem ser organizados tanto pelo **Melhor Preço** quanto pelo **Mais Próximo** (usando algoritmo de cálculo de distância do usuário).
- **Destaque Visual de Economia**: Algoritmo global que varre os produtos das lojas concorrentes e estampa o highlight **"OFERTA"** ou a tag condicional **"O MELHOR PREÇO"** na melhor oportunidade matemática para o cliente.

### 2. Tela de Detalhe de Produto (Marketplace Profile)
- Inspirado no Mercado Livre (Buybox). Apresenta a foto maximizada do item, a loja padrão vencedora e informações gerais.
- **Comparador Paralelo**: Exibe uma lista de todos os **"Outros vendedores"** contendo o exato mesmo produto, mostrando a diferença de preços.

### 3. Tela da Loja (Store Profile)
- Carrega um cabeçalho cinemático isolando o nome, foto, rating (estrelas) e custo de frete do Comércio escolhido.
- Exibe o portfólio completo de mercadorias apenas desta loja na vitrine abaixo do cabeçalho.

---

## 🛠️ Tecnologias e Stack (CDN)

A aplicação foi montada sem bundlers (como Vite ou Webpack) de forma proposital para testes práticos de design e conceito isolados no arquivo HTML:
- **[React](https://reactjs.org/) & [React DOM](https://reactjs.org/docs/react-dom.html)**: Importados via CDN (`v18.x`).
- **[Babel Standalone](https://babeljs.io/)**: Compila as tags JSX criadas nos fluxos de componentes diretamente na runtime do navegador.
- **[Tailwind CSS](https://tailwindcss.com/)**: Motor de estilos importado via script para construção avançada da UI (glassmorphism flex, grids complexos e cores premium) com flexibilidade In-Browser. 
- Fotos ilustrativas fornecidas via Unsplash / SVGs Heroicons nativizados na renderização via `const Icon`.

---

## 💻 Como Rodar Esse Projeto

Por ser um projeto Autossuficiente, é incrivelmente fácil de lançar e testar:

1. Faça o Clone/Download do arquivo em seu sistema;
2. Navegue até a pasta pelo seu explorador de arquivos;
3. Dê um duplo-clique no arquivo `index.html`. 

*(Sério, é isso. Ele vai abrir em seu navegador padrão Safari, Edge, ou Chrome pronto para interagir visualmente).*

---

### *Próximos Passos (Evolução Técnica Sugerida)*
- Separação dos Componentes e Migração do projeto para um Framework definitivo como *React Native (Expo)*, *Vite* ou *Next.js*.
- Substituição dos dados Mocados por API conectada em um banco *Firebase*, *PostgreSQL* ou *MongoDB*.
- Consumir Geolocation API nativa para trocar distâncias estáticas por travas de raio reais do dispositivo do usuário.
