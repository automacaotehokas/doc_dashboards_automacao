# Conceitos e Indicadores do MAPA  

## **1. Introdução**  
Os indicadores abaixo avaliam a **robustez da programação semanal** a partir de três perspectivas:  

1. **Variação pelo olhar do cliente** (Data Repactuada)  
2. **Variação em relação às datas anteriores** (Histórico de reprogramações)  
3. **Variação contra a primeira data publicada** (Data Inicial)  

**Objetivo:**  
- Gerar insights para **gestão de contratos** (repactuações com clientes).  
- Apoiar a **logística** no realinhamento de trâmites.  
- Identificar OPs com desvios críticos.  

---

## **2. Indicadores**  

### **2.1 Variação Mapa Atual x Anterior (GAP MAPA ANTERIOR)**  
- **O que mede:** Quantidade de reprogramações sofridas por uma OP.  
- **Cálculo:** Diferença entre a última data programada e a versão anterior do MAPA.  
- **Uso:** Identifica instabilidade na programação.  

### **2.2 Variação Mapa Atual x Data Repac (GAP REPAC)**  
- **O que mede:** Desvio entre a data atual e o acordado com o cliente (repactuada/contratual).  
- **Cálculo:** Última data programada vs. Data Repactuada.  
- **Uso:** Prioriza OPs que exigem ação comercial ou logística.  

### **2.3 Variação Mapa Atual x Inicial (GAP INICIAL)**  
- **O que mede:** Mudança em relação primeira programação.  
- **Cálculo:** Última data programada vs. Primeira Data informada no TrackFlow.  
- **Uso:** Avalia impacto global do planejamento.  

---

## **3. Classificação por Status**  
Baseado nos GAPs, cada OP recebe um status:  

| **Status**          | **Condição**                                  | **Ação Recomendada**                  |  
|---------------------|----------------------------------------------|---------------------------------------|  
| **Data Não Atende** | Data programada > Data Repactuada           | Contatar cliente para repactuação.    |  
| **Reprogramada**    | Houve variação (adianto/atraso) vs. anterior | Ajustar logística ou recursos.        |  
| **Falta Data PCP**  | OP em fabricação sem data programada        | Urgência: inserir no MAPA.            |  
| **Data Atende**     | Data programada ≤ Data Repactuada           | Manter monitoramento.                 |  

---

## **4. Próximos Passos**  
Para aplicar essa análise na rotina padrão, acesse o guia:  
[**Rotina de Análise do MAPA**](reuniao_mapa.md)  