# LogiSmart
Dashboard completo para gestão logística em tempo real, desenvolvido com foco em análise de dados,  otimização de rotas e monitoramento de frota.

🚛 LogiSmart - Dashboard de Logística Inteligente
📋 Sobre o Projeto
Dashboard completo para gestão logística em tempo real, desenvolvido com foco em análise de dados, otimização de rotas e monitoramento de frota. Ideal para empresas de transporte, e-commerce e operações logísticas.
🎯 Funcionalidades Principais
📍 Mapa Interativo

Visualização de entregas em tempo real
Marcadores coloridos por status de entrega
Popup com informações detalhadas de cada ponto
Integração com OpenStreetMap (API gratuita)

📊 Métricas em Tempo Real

Entregas do Dia: Contador total de entregas realizadas
Entregas Pendentes: Monitoramento de entregas em aberto
Tempo Médio: Cálculo automático do tempo médio de entrega
Eficiência: Percentual de performance da operação

🚛 Monitoramento de Frota

Status em tempo real de cada veículo
Monitoramento de níveis de combustível
Alertas automáticos para manutenção
Sistema de cores para priorização

📈 Análises e Relatórios

Gráficos de performance semanal
Análise de tendências
Comparativos históricos

🔮 Previsões Inteligentes

Análise preditiva de demanda
Sugestões de otimização de rotas
Alertas de manutenção preventiva
Estimativas de picos de demanda

✅ Plano de Ação

Tarefas prioritárias das próximas 24h
Sistema de priorização (Alta/Média/Baixa)
Cronograma organizado por horários

🔧 Arquitetura Técnica
Frontend
├── HTML5 Semântico
├── CSS3 Moderno (Flexbox/Grid)
├── JavaScript Vanilla (ES6+)
├── Leaflet.js (Mapas)
├── Chart.js (Gráficos)
├── Font Awesome (Ícones)
└── Design Responsivo
Lógica de Dados
Estrutura de Dados Principal
javascriptdeliveryData = {
    totalDeliveries: Number,    // Total de entregas
    pendingDeliveries: Number,  // Entregas pendentes
    avgTime: Number,           // Tempo médio em minutos
    efficiency: Number,        // Percentual de eficiência
    fleetStatus: Array,        // Status da frota
    predictions: Array,        // Previsões geradas
    actionPlan: Array         // Plano de ação
}
Pontos de Entrega (Geolocalização)
javascriptdeliveryPoints = [
    {
        lat: Number,           // Latitude
        lng: Number,           // Longitude
        status: String,        // Status da entrega
        address: String        // Endereço
    }
]
Funções Principais
1. updateDashboard()
javascript// Função principal de atualização
- Gera dados simulados em tempo real
- Atualiza todas as métricas
- Chama subfunções de atualização
- Executa a cada 30 segundos
2. addMarkersToMap()
javascript// Gerenciamento do mapa
- Adiciona marcadores coloridos
- Define popups informativos
- Sistema de cores por status
- Integração com Leaflet.js
3. updateFleetStatus()
javascript// Monitoramento da frota
- Atualiza status dos veículos
- Monitora níveis de combustível
- Gera alertas automáticos
- Aplica classes CSS por prioridade
4. updatePredictions()
javascript// Sistema de previsões
- Análise preditiva básica
- Cálculos de otimização
- Geração de insights
- Estimativas de confiança
5. updateActionPlan()
javascript// Plano de ação dinâmico
- Priorização de tarefas
- Organização temporal
- Sistema de cores
- Interface intuitiva
📊 Origem e Tratamento dos Dados
Dados Simulados (Demonstração)
javascript// Geração aleatória para demonstração
Math.floor(Math.random() * 100) + 50  // Entregas
Math.floor(Math.random() * 20) + 5   // Pendentes
Math.floor(Math.random() * 30) + 15  // Tempo médio
Math.floor(Math.random() * 20) + 80  // Eficiência
Preparação para Dados Reais
APIs Recomendadas:

Correios: Rastreamento de encomendas
Google Maps: Geolocalização e rotas
OpenWeather: Condições climáticas
Fuel API: Preços de combustível
Fleet Management: Dados de frota

Estrutura para APIs Reais:
javascript// Exemplo de integração
async function fetchRealData() {
    try {
        const response = await fetch('API_ENDPOINT');
        const data = await response.json();
        return processData(data);
    } catch (error) {
        console.error('Erro ao buscar dados:', error);
        return fallbackData();
    }
}
🔄 Sistema de Atualização
Atualização Automática
javascript// Executa a cada 30 segundos
setInterval(updateDashboard, 30000);

// Timestamp visual
document.getElementById('lastUpdate').textContent = 
    new Date().toLocaleTimeString('pt-BR');
Indicador Visual

Animação CSS de "pulse" no indicador
Timestamp da última atualização
Status visual de "Atualizando..."

🎨 Design e UX
Princípios Aplicados

Glassmorphism: Efeitos de vidro modernos
Design Responsivo: Mobile-first approach
Micro-interações: Hover effects e transições
Hierarquia Visual: Cores e tipografia consistentes

Paleta de Cores
cssPrimary: #667eea (Azul principal)
Secondary: #764ba2 (Roxo secundário)
Success: #28a745 (Verde)
Warning: #ffc107 (Amarelo)
Danger: #dc3545 (Vermelho)
🚀 Como Executar
Método 1: Local
bash# Clone o repositório
git clone [seu-repositorio]

# Abra o arquivo
open index.html
Método 2: GitHub Pages

Ative GitHub Pages no repositório
Acesse: https://[seu-usuario].github.io/[nome-repo]

Método 3: Live Server (VS Code)
bash# Instale a extensão Live Server
# Clique com botão direito no index.html
# Selecione "Open with Live Server"
📱 Responsividade
Breakpoints
cssDesktop: > 768px (Grid 2 colunas)
Tablet/Mobile: ≤ 768px (Grid 1 coluna)
Adaptações Mobile

Layout em coluna única
Botões maiores para touch
Fonte ajustada para legibilidade
Mapas otimizados para mobile

🔧 Tecnologias Utilizadas
TecnologiaVersãoFunçãoHTML5-Estrutura semânticaCSS3-Estilização modernaJavaScriptES6+Lógica e interatividadeLeaflet.js1.9.4Mapas interativosChart.js4.0+Gráficos e visualizaçõesFont Awesome6.0.0Ícones vetoriais
🔮 Evolução do Projeto
Próximas Implementações

 Backend com Node.js
 Banco de dados (MongoDB/PostgreSQL)
 APIs reais de rastreamento
 Autenticação de usuários
 Relatórios em PDF
 Notificações push
 Machine Learning para previsões
 App mobile (React Native)

Integrações Planejadas

Sistema ERP existente
APIs de transportadoras
Pagamentos online
CRM empresarial
Sistemas de estoque

📈 Métricas de Performance
Otimizações Implementadas

Lazy loading para gráficos
Debounce em atualizações
Cache de dados locais
Compressão de imagens
Minificação de CSS/JS

Monitoramento

Tempo de carregamento < 3s
Responsividade garantida
Compatibilidade cross-browser
Acessibilidade (WCAG)

🤝 Contribuição
Como Contribuir

Fork do projeto
Crie uma branch para sua feature
Commit suas mudanças
Push para a branch
Abra um Pull Request

Padrões de Código

ES6+ JavaScript
Comentários em português
Nomenclatura descritiva
Indentação 4 espaços

📞 Contato
Desenvolvedor: [Seu Nome]
LinkedIn: [Seu LinkedIn]
Email: [Seu Email]
Portfolio: [Seu Portfolio]

🎓 Demonstração de Conhecimentos
Este projeto demonstra domínio em:
Frontend

HTML5 semântico e acessível
CSS3 moderno (Grid, Flexbox, Animations)
JavaScript ES6+ (Async/Await, Promises, Modules)
APIs externas (Leaflet, Chart.js)
Design responsivo e mobile-first

Lógica de Programação

Manipulação de DOM
Gerenciamento de estado
Funções puras e modulares
Tratamento de erros
Otimização de performance

UX/UI Design

Prototipagem e wireframing
Hierarquia visual
Micro-interações
Acessibilidade
Design system consistente

Análise de Dados

Visualização de dados
Métricas de performance
Análise preditiva básica
KPIs de logística
Relatórios automáticos

Conhecimento de Negócio

Processos logísticos
Gestão de frota
Otimização de rotas
Análise de custos
Indicadores de performance


Dashboard desenvolvido para demonstrar habilidades em desenvolvimento frontend, análise de dados e conhecimento do setor logístico.
