# 📊 Aprendizado de Máquina Não Supervisionado
### Brazil Organized Violence (1993–2024)
Projeto final de disciplina focado na aplicação prática de técnicas de aprendizado não supervisionado para análise exploratória e descoberta de padrões em dados reais de conflitos violentos no Brasil.

---
### 🎯 Objetivo do Projeto
O objetivo deste projeto é explorar, reduzir dimensionalidade e agrupar padrões de violência organizada no Brasil utilizando algoritmos clássicos de aprendizado não supervisionado. A ideia central é responder perguntas como:

---
## 📁 Dataset

**Fonte:** Kaggle  
**Nome:** *Brazil Organized Violence (1993–2024)*  

O dataset documenta conflitos violentos organizados no Brasil entre **1993 e 2024**, contendo informações detalhadas sobre eventos de violência, incluindo atores envolvidos, localização geográfica, tipo de conflito e número de fatalidades.

### 📌 Principais Grupos de Variáveis

Para fins de aprendizado não supervisionado, as variáveis do dataset podem ser organizadas conceitualmente em grupos:

#### 1. Variáveis Temporais
- `year`
- `date_start`, `date_end`
- `active_year`
- `date_prec`

#### 2. Variáveis Espaciais / Geográficas
- `latitude`, `longitude`
- `adm_1` (estado)
- `adm_2` (município)
- `where_prec`
- `priogrid_gid`

#### 3. Características do Conflito
- `type_of_violence` (1 = estatal, 2 = não estatal, 3 = violência unilateral)
- `event_clarity`
- `number_of_sources`

#### 4. Impacto / Intensidade da Violência
- `deaths_a`
- `deaths_b`
- `deaths_civilians`
- `deaths_unknown`
- `best`, `high`, `low`

#### 5. Metadados e Identificadores (não utilizados diretamente)
- `id`, `relid`, `conflict_new_id`, `dyad_new_id`
- Nomes de atores (`side_a`, `side_b`)
- Campos textuais descritivos de fontes e localização

> ⚠️ **Observação:** variáveis textuais extensas, identificadores e campos puramente descritivos são excluídos ou agregados durante o pré-processamento, pois não contribuem diretamente para métodos baseados em distância.

---

## Em construção 🚧