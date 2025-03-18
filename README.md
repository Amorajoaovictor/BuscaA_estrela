## Requisitos 
### 1.  Obtenção dos Dados do OpenStreetMap🗺️ 
procedimento básico envolve:
- Baixar um subgrafo de OSM para uma cidade ou bairro específico.
- Filtrar apenas os nós e arestas relevantes para a navegação. - Criar um grafo onde os vértices representam cruzamentos e as arestas representam ruas com um peso associado (distância ou tempo estimado).

### 2. Modelagem do Problema como Busca no Espaço de Estados ❓
Cada estado no espaço de busca será um nó do grafo (interseção de ruas). As transições 
entre estados ocorrem ao percorrer as ruas (arestas). deve ser definido: 
- Espaço de estados: conjunto de interseções. - Operadores de transição: deslocamento de um nó para outro através de uma rua. 
- Função de custo g(n): distância percorrida ou tempo estimado. 
- Estado objetivo: o nó correspondente ao destino. - Heurísticas h(n): estimativas do custo restante até o destino.
### 3. Implementação do Algoritmo A* 👨‍💻
Os alunos devem implementar a busca A* utilizando uma fila de prioridade para explorar os 
caminhos de menor custo primeiro. A função de avaliação será: 
f(n) = g(n) + h(n) 
onde: - g(n): custo real acumulado do início até o nó atual. - h(n): heurística estimando o custo restante até o destino. 
Devem ser testadas duas heurísticas diferentes: 
1. Distância Euclidiana (considera apenas a distância em linha reta entre os nós). 
2. Distância Geodésica (Haversine) (considera a curvatura da Terra para uma melhor 
aproximação da distância).
