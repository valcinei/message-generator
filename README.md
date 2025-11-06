# 🎉 Gerador de Mensagens Personalizadas para WhatsApp

Um gerador universal de mensagens personalizado para envio via WhatsApp, **100% customizável** e compatível com GitHub Pages.

## 🚀 Funcionalidades Principais

### ✨ **Variáveis Dinâmicas**
- **Defina suas próprias variáveis** - Nome, telefone, produto, valor, data, etc.
- **Tipos personalizáveis** - text, number, date
- **Campos obrigatórios** configuráveis
- **Reordenação** das variáveis por drag & drop
- **Formatação automática** de valores monetários

### 🎨 **Interface Moderna**
- **🌙 Tema escuro/claro** - Detecção automática do sistema + escolha manual
- **📱 Bootstrap 5** - Interface responsiva e componentes modernos
- **🎯 Ícones Bootstrap** - Interface visual intuitiva
- **💫 Animações suaves** - Transições e feedback visual
- **🔄 Contraste otimizado** - Textos legíveis em ambos os temas
- **📱 PWA Ready** - Suporte a aplicativo web progressivo

### 📥 **Importação Flexível**
- **📊 CSV** - Formato tradicional com detecção automática de colunas
- **📋 JSON** - Arrays, objetos ou configurações completas
- **🔧 Auto-detecção** - Criação automática de variáveis conforme dados
- **🎯 Tipos inteligentes** - Detecção automática de number/date/text

### 💾 **Configurações Discretas**
- **📦 Dropdown compacto** - Economiza espaço na interface
- **⚡ Acesso rápido** - Ações principais sempre visíveis
- **📊 Contador visual** - Badge mostra quantidade de configs salvas
- **🎯 UX otimizada** - Interface limpa e funcional

### 🎯 **Casos de Uso Diversos**
- **E-commerce**: Confirmação de pedidos, promoções
- **Serviços**: Agendamentos, lembretes
- **Cashback**: Notificações de crédito
- **Marketing**: Campanhas personalizadas
- **Suporte**: Mensagens de atendimento
- **Eventos**: Convites e confirmações

### 💾 **Persistência Inteligente**
- **Auto-save automático** das configurações e dados
- **Configurações nomeadas** para diferentes campanhas
- **Backup/Restore** completo em JSON
- **Import/Export** de arquivos
- **Armazenamento local** (localStorage) - sem servidor

### 📱 **Compatibilidade Total**
- **GitHub Pages ready** - 100% estático, arquivo único
- **Responsivo** para todos os dispositivos
- **Offline-first** - funciona sem internet
- **Cross-browser** - navegadores modernos

## 🔧 Como Usar

### 1. **🎨 Personalizar Interface**
- **🔄 Detecção automática**: O tema segue automaticamente a preferência do sistema (escuro/claro)
- **🎯 Escolha manual**: Clique no botão 🌙/☀️ no canto superior direito para forçar um tema
- **💡 Indicador**: Quando segue o sistema, aparece um ponto azul no botão
- **💾 Persistência**: Sua escolha manual é salva e tem prioridade sobre o sistema

### 2. **📝 Definir Variáveis**
1. Clique em **"+ Adicionar Variável"** para criar campos personalizados
2. Configure **nome**, **label** e **tipo** (text/number/date)
3. As variáveis aparecerão automaticamente na tabela
4. Use **"Carregar exemplo"** para ver uma configuração pronta

### 3. **📥 Importar Dados**
- **CSV**: Formato tradicional com detecção de cabeçalho
- **JSON**: Arrays, objetos ou configurações completas
- **Auto-detecção**: Criação automática de variáveis
- **Tipos inteligentes**: number/date detectados automaticamente

### 4. **⚙️ Configurar Template**
1. Digite sua mensagem usando `{{nome_da_variavel}}`
2. Configure o **nome da campanha/empresa**
3. Escolha qual campo será usado como **telefone**
4. Visualize as **variáveis disponíveis** em tempo real

### 5. **💾 Gerenciar Configurações**
- **Dropdown discreto**: Clique em "Configurações Salvas"
- **Salvar**: Botão "Salvar configuração" 
- **Carregar**: Clique no ícone ⬇️ na configuração desejada
- **Backup**: Botões de importar/exportar no dropdown

### 6. **🚀 Gerar e Enviar**
1. Clique em **"Gerar mensagens"**
2. Use **"WhatsApp"** para envio direto
3. Use **"Copiar"** para outros canais

## 🎨 Sistema de Variáveis

### **Variáveis Padrão**
- `{{nome}}` - Nome completo
- `{{telefone}}` - Telefone normalizado
- `{{campanha}}` - Nome da campanha/empresa
- `{{primeiro_nome}}` - Primeiro nome extraído automaticamente

### **Variáveis Personalizadas**
Crie quantas quiser:
- `{{produto}}`, `{{servico}}`, `{{evento}}`
- `{{valor}}`, `{{preco}}`, `{{desconto}}` (formatação automática BRL)
- `{{data}}`, `{{prazo}}`, `{{vencimento}}`
- `{{codigo}}`, `{{cupom}}`, `{{referencia}}`

### **Formatação Automática**
- **Valores monetários**: Variáveis com "valor", "preco", "cashback" são formatadas em BRL
- **Telefones**: Normalização automática para formato internacional
- **Primeiro nome**: Extraído automaticamente da variável "nome"

## � **Formatos de Importação**

### **📊 CSV**
```csv
nome,telefone,produto,valor
João Silva,(11) 99999-1111,Smartphone,1299.99
Maria Santos,(21) 88888-2222,Notebook,2499.00
```

### **📋 JSON - Array Simples**
```json
[
  {
    "nome": "João Silva",
    "telefone": "(11) 99999-1111", 
    "produto": "Smartphone Pro",
    "valor": 1299.99
  }
]
```

### **🔧 JSON - Configuração Completa**
```json
{
  "nomeCampanha": "Black Friday 2024",
  "variaveis": [
    {"nome": "nome", "label": "Nome", "tipo": "text"},
    {"nome": "produto", "label": "Produto", "tipo": "text"},
    {"nome": "valor", "label": "Valor", "tipo": "number"}
  ],
  "template": "Olá {{nome}}! Seu {{produto}} por {{valor}}...",
  "registros": [...]
}
```

### **📦 JSON - Objeto Chave-Valor**
```json
{
  "cliente1": {"telefone": "11999999999", "produto": "A"},
  "cliente2": {"telefone": "21888888888", "produto": "B"}
}
```

## 📞 **Formato de Telefone**

Aceita vários formatos e normaliza automaticamente:
- `(92) 9 8888-1111` → `5592988881111`
- `92 99999-2222` → `5592999992222`  
- `11 97654-3333` → `5511976543333`

## 💾 **Gerenciamento de Dados**

### **Auto-save Inteligente**
- Salva automaticamente a cada mudança (1 segundo de delay)
- Restaura automaticamente ao recarregar a página
- Indicador visual quando dados são salvos

### **Configurações Nomeadas**
- Salve diferentes configurações para campanhas distintas
- Carregue rapidamente configurações salvas
- Exclua configurações desnecessárias
- Histórico com data/hora de cada configuração

### **Backup/Restore**
- **Exportar**: Baixa arquivo JSON com todos os dados
- **Importar**: Restaura dados de arquivo de backup
- **Formato**: JSON estruturado e legível
- **Portabilidade**: Transfira dados entre dispositivos

### **Import CSV Inteligente**
- **Detecção automática** de colunas
- **Criação dinâmica** de variáveis conforme CSV
- **Flexibilidade total** - qualquer estrutura de dados
- **Mapeamento automático** para variáveis existentes

## 🌐 **Deploy no GitHub Pages**

### **Arquivo Único**
Este projeto foi otimizado para ser **apenas um arquivo**: `index.html`

### **Setup Simples**
1. Faça fork/clone deste repositório
2. Vá em `Settings` → `Pages` no GitHub
3. Selecione `Deploy from a branch`
4. Escolha `main` branch
5. Clique em `Save`

### **Acesso Direto**
- Seu site estará disponível em: `https://[username].github.io/[repository-name]/`
- Funciona imediatamente, sem configuração adicional

## 🎯 **Casos de Uso Reais**

### **Loja Online**
```csv
nome,telefone,produto,valor,codigo
Ana Silva,(11) 99999-1111,Vestido Azul,89.90,PED001
Bruno Costa,(21) 88888-2222,Sapato Social,199.00,PED002
```

### **Clínica Médica**
```csv
nome,telefone,consulta,data,horario,doutor
Maria Santos,(85) 77777-3333,Dermatologia,15/12/2024,14:30,Dr. João
Pedro Lima,(62) 66666-4444,Cardiologia,16/12/2024,09:00,Dra. Ana
```

### **Evento/Workshop**
```csv
nome,telefone,evento,data,local,valor
Carlos Souza,(31) 55555-5555,Workshop React,20/12/2024,Online,150.00
Lucia Mendes,(48) 44444-6666,Curso JavaScript,22/12/2024,Presencial,250.00
```

## 🔒 **Privacidade e Segurança**

- **100% client-side**: Nenhum dado é enviado para servidores
- **localStorage apenas**: Dados ficam apenas no seu navegador
- **Sem tracking**: Não há coleta de dados ou analytics
- **Código aberto**: Todo o código é transparente e auditável
- **Sem dependências**: JavaScript puro, sem bibliotecas externas

## 🛠️ **Tecnologias**

- **HTML5** - Estrutura semântica
- **CSS3** - Design responsivo e moderno  
- **Vanilla JavaScript** - Funcionalidades sem dependências
- **LocalStorage API** - Persistência local
- **File API** - Import/Export de arquivos
- **Clipboard API** - Cópia de mensagens

## ⚡ **Performance**

- **Carregamento rápido** - Arquivo único otimizado
- **Responsividade** - Interface fluida em qualquer dispositivo
- **Offline-first** - Funciona sem conexão após primeiro carregamento
- **Auto-save eficiente** - Debounce para evitar salvamentos desnecessários

## 🎨 **Interface**

- **Design moderno** - Dark theme profissional
- **UX intuitiva** - Fluxo de trabalho claro e direto
- **Responsiva** - Mobile-first design
- **Acessível** - Semântica HTML adequada

## 📝 **Licença**

Este projeto é open source e está disponível sob a licença MIT.

## 🤝 **Contribuição**

Contribuições são bem-vindas! Sinta-se à vontade para:
- Abrir issues para bugs ou sugestões
- Fazer pull requests com melhorias
- Compartilhar feedback sobre a ferramenta
- Criar templates de exemplo
- Melhorar a documentação

## 🚀 **Próximas Funcionalidades**

- [ ] Drag & drop para reordenar variáveis
- [ ] Templates pré-definidos por categoria
- [ ] Validação avançada de campos
- [ ] Exportação para outros formatos
- [ ] Integração com APIs de WhatsApp Business
- [ ] Agendamento de mensagens
- [ ] Analytics de engajamento

---

**✨ Desenvolvido para facilitar a comunicação personalizada via WhatsApp de forma eficiente e profissional** 🚀

### 📊 **Estatísticas do Projeto**
- **1 arquivo único** - Máxima simplicidade
- **0 dependências** - 100% autônomo
- **100% offline** - Funciona sem internet
- **∞ possibilidades** - Variáveis ilimitadas e personalizáveis