# Licenças PAC - Sistema de Gestão e Monitoramento de Licenciamento Ambiental

O **Licenças PAC** é uma plataforma web moderna, colaborativa e 100% baseada em nuvem, desenvolvida especialmente para a Secretaria Especial do Programa de Aceleração do Crescimento (**Novo PAC / Casa Civil da Presidência da República**).

O sistema unifica a **Tabela Mestra (Técnica/Operacional)** e a **Tabela Executiva (Diretoria/Ministros)** em uma única fonte de dados inteligente e em tempo real.

---

## 🌟 Principais Recursos e Premissas Atendidas

### 1. Tabela Interativa Semelhante ao Excel / Google Sheets
- **Edição Inline Direta:** Dê duplo clique em qualquer célula da tabela para editar diretamente no navegador.
- **Filtros Multi-critério:** Filtre instantaneamente por Subeixo (*Rodovias*, *Ferrovias*, *Infraestrutura Hídrica*), Status da Licença (*Sem LP*, *LP*, *LI*, *LO*), Órgão Pendente (*IBAMA*, *FUNAI*, *INCRA*, *IPHAN*, *ICMBio*, *DNIT*, etc.) e Projetos Prioritários.
- **Busca Rápida Global:** Pesquise por rodovia, número de processo SEI ou termos-chave nas providências.

### 2. Colaboração em Tempo Real (Multi-User Real-Time)
- **Sincronização Instantânea:** Alterações feitas por qualquer membro da equipe são propagadas em tempo real entre todas as abas e sessões ativas via `BroadcastChannel` e armazenamento local sincronizado.
- **Presença Ativa da Equipe:** Avatares no cabeçalho indicam visualmente os membros conectados e atuando na base de dados.
- **Prevenção de Conflitos:** Atualizações atômicas em nível de campo.

### 3. Controle de Prazos e Órgãos Intervenientes Federais
- **Monitoramento de Órgãos:** Acompanhamento rigoroso de prazos com IBAMA, FUNAI, INCRA, IPHAN, ICMBio e órgãos estaduais (FEMARH, SETRANS, INEMA).
- **Classificação de Criticidade:**
  - 🔴 **Vencidos:** Providências com prazo expirado necessitando de cobrança imediata em Sala de Situação.
  - 🟡 **Atenção (15 dias):** Prazos próximos ao vencimento para atuação preventiva.
  - 🟢 **No Prazo:** Estudos e análises em andamento regular.
  - ⚪ **A Definir:** Demandas dependentes de definição de novas tratativas.
- **Painel Analítico:** Gráficos de distribuição percentual de pendências por órgão e feed ordenado de próximos prazos.

### 4. Auto-Preenchimento e Rastreamento Inteligente
- **Carimbo "Modificado em":** Atualizado automaticamente com a data corrente (`DD/MM/YYYY`) sempre que qualquer dado do processo for alterado.
- **Extração Automática de Órgãos ("Pendência"):** Motor de processamento textual que analisa os comentários e providências digitados e infere automaticamente os órgãos envolvidos (ex: detecta `"DNIT"` e `"FUNAI"` no texto e gera `"DNIT e FUNAI"` na coluna de Pendência).

### 5. Legenda e Regras de Cores Automáticas
- Aplicação visual imediata baseada nas licenças cadastradas:
  - 🔴 **Sem Licença Prévia:** Destaque em vermelho e sublinhado para projetos prioritários.
  - 🔵 **Com Licença Prévia (LP):** Indicador visual azul claro.
  - 🟢 **Com Licença de Instalação (LI):** Indicador visual verde claro.
  - 🟣 **Com Licença de Operação (LO):** Indicador visual roxo/dourado.

### 6. Geração Inteligente de "Riscos e Oportunidades"
- **Auto-Síntese Executiva:** Motor de síntese que lê o histórico detalhado dos comentários e providências técnicas e gera automaticamente o texto conciso e direto para a coluna "Riscos e Oportunidades" da Tabela Executiva.
- Botão **"Auto-Síntese Executiva"** no topo para atualizar todos os processos em lote com 1 clique.

### 7. View Executiva e Exportação em PDF Padrão Ministerial
- **Alternância de Visões em 1 Clique:**
  - *1. Tabela Mestra:* Visão completa com 15 colunas técnicas (Processos, TRs, LPs, LIs, LOs).
  - *2. Tabela Executiva:* Formato idêntico ao modelo oficial da Casa Civil / Novo PAC.
  - *3. Painel de Prazos:* Dashboard de governança e intervenientes.
- **Exportação PDF de Alta Fidelidade:** Botão "Exportar PDF Executivo" que gera um documento A4 Paisagem formatado com cabeçalho oficial da Casa Civil / Presidência da República, barra de legendas, tabelas paginadas e carimbo de data.

### 8. Aplicação 100% em Nuvem
- Acessível diretamente pelo navegador web (Google Chrome, Microsoft Edge, Safari, Firefox) sem necessidade de instalação de softwares ou plugins adicionais.

---

## 🚀 Como Executar e Utilizar

### Execução Local Rápida:
Basta abrir o arquivo `index.html` em qualquer navegador web moderno:
```bash
open /Users/ligiamoreiradealmeida/.gemini/antigravity/scratch/licencas-pac/index.html
```

### Hospedagem em Nuvem:
Por ser uma Single-Page Application (SPA) pura com zero dependências externas bloqueadas:
1. **Gov.br / Dataprev / Serpro:** Pode ser hospedada diretamente em containers Docker Nginx ou buckets S3/Object Storage corporativos.
2. **GitHub Pages / Vercel / Netlify / AWS CloudFront:** Faça o deploy da pasta com 1 clique.

