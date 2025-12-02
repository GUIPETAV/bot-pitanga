# 🏢 TypeBot - Condomínio Vista de Pitanga

Bot de atendimento automatizado para o Condomínio Vista de Pitanga. 

## 📋 Funcionalidades

- 🏊 **Reserva de Pulseiras da Piscina** - Com limite de 6 pulseiras/mês por morador
- 🚪 **Contato com Porteiro** - Redirecionamento para WhatsApp
- 👔 **Contato com Síndico** - Redirecionamento para WhatsApp

## 🚀 Como usar

### 1. Importar no TypeBot. io

1. Acesse [typebot.io](https://typebot.io)
2. Faça login na sua conta
3. Clique em **"Create a typebot"**
4. Selecione **"Import a file"**
5. Faça upload do arquivo `typebot-vista-pitanga.json`
6. Pronto!  Seu bot está configurado

### 2. Configurar números de WhatsApp

Após importar, edite os blocos de **Porteiro** e **Síndico**:

1. Clique no grupo "Falar com Porteiro" ou "Falar com Síndico"
2. Edite o link do WhatsApp, substituindo `5500000000000` pelo número real
3. Formato: `55` + DDD + número (ex: `5511999999999`)

### 3.  Configurar integração com Google Sheets

Para exportar os dados das reservas para uma planilha:

#### Passo 1: Criar a planilha
Crie uma planilha no Google Sheets com as seguintes colunas:
| A | B | C | D | E | F | G |
|---|---|---|---|---|---|---|
| Timestamp | Nome | Bloco | Apartamento | Data Reserva | Qtd Pulseiras | Mês/Ano |

#### Passo 2: Conectar no TypeBot
1. No TypeBot, vá até o bloco de **webhook** no grupo "Reserva Confirmada"
2. Use a integração nativa com Google Sheets ou
3. Configure um webhook com Make/Zapier para enviar os dados

## ⚙️ Configurações do Bot

| Configuração | Valor |
|--------------|-------|
| Limite de pulseiras | 6 por pessoa/mês |
| Horário da piscina | 8h às 22h |
| Dados coletados | Nome, Bloco, Apto, Data, Quantidade |

## 📊 Controle de Limite Mensal

O bot pergunta ao morador quantas pulseiras já foram usadas no mês atual. 
- Se já usou **6 pulseiras**, a reserva é bloqueada
- Para um controle mais preciso, configure a planilha para consultar automaticamente

## 📝 Estrutura dos Arquivos

```
bot-pitanga/
├── README.md                    # Este arquivo
├── typebot-vista-pitanga.json   # Arquivo para importar no TypeBot.io
└── planilha-modelo.md           # Estrutura da planilha de controle
```

## 🔧 Personalização

### Alterar limite de pulseiras
No arquivo JSON, procure por "6 pulseiras" e altere conforme necessário.

### Adicionar mais opções ao menu
Edite o grupo "Boas-vindas" e adicione novos itens no bloco de escolha.

### Alterar horário da piscina
Procure por "8h às 22h" no JSON e altere para o horário desejado.

## 📞 Suporte

Para dúvidas sobre o TypeBot. io, acesse: [docs.typebot.io](https://docs.typebot.io)