# 📊 Modelo de Planilha - Controle de Pulseiras

## Estrutura das Colunas

| Coluna | Nome | Descrição | Exemplo |
|--------|------|-----------|---------|
| A | **Timestamp** | Data/hora do registro | 02/12/2025 14:30:00 |
| B | **Nome** | Nome completo do morador | João Silva |
| C | **Bloco** | Bloco do apartamento | A |
| D | **Apartamento** | Número do apartamento | 101 |
| E | **Data Reserva** | Data da reserva | 05/12/2025 |
| F | **Qtd Pulseiras** | Quantidade reservada | 4 |
| G | **Mês/Ano** | Mês e ano para controle | 12/2025 |

## Fórmulas Úteis

### Contar pulseiras usadas por morador no mês atual
```
=SUMIFS(F:F, B:B, "Nome do Morador", G:G, TEXT(TODAY(),"MM/YYYY"))
```

### Verificar se morador atingiu o limite
```
=IF(SUMIFS(F:F, B:B, B2, G:G, G2)>6, "LIMITE ATINGIDO", "OK")
```

## Exemplo de Dados

| Timestamp | Nome | Bloco | Apto | Data Reserva | Qtd | Mês/Ano |
|-----------|------|-------|------|--------------|-----|---------|
| 02/12/2025 10:00 | Maria Santos | B | 202 | 03/12/2025 | 2 | 12/2025 |
| 02/12/2025 11:30 | João Silva | A | 101 | 04/12/2025 | 4 | 12/2025 |
| 02/12/2025 14:00 | Maria Santos | B | 202 | 10/12/2025 | 3 | 12/2025 |