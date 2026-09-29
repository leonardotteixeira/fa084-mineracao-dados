# FA084 — Mineração de Dados

Aluno: Leonardo Teixeira  
RA: 245602  
UNICAMP

## Algoritmo Genético — Alocação de Grade de Disciplinas

O objetivo é montar uma grade semanal de disciplinas (segunda a sexta, uma disciplina por dia) com o menor custo possível, usando um algoritmo genético.

Cada solução (cromossomo) indica o professor e a disciplina de cada dia. A função de fitness soma o custo dos professores alocados e aplica as penalidades do enunciado:

- ×2 se o professor nunca ministrou a disciplina;
- ×1,5 se um professor se repete;
- ×5 se uma disciplina se repete.

O notebook:

- monta o arquivo `tab_professores.txt` e o lê para um dicionário;
- implementa a função de fitness, a mutação (1 gene por vez), o cruzamento (ponto de corte variável) e o algoritmo genético;
- demonstra o ótimo global do problema (F\* = 314), que serve para avaliar os resultados do algoritmo;
- executa a configuração oficial: cromossomo inicial do enunciado, população 60, elitismo 20%, mutação 10%, 500 gerações;
- estuda o efeito dos parâmetros e compara a configuração oficial com uma configuração proposta, em 30 execuções com sementes fixas.

## Estrutura

```
fa084-mineracao-dados/
├── README.md
├── algoritmo_genetico_grade_disciplinas_entrega.ipynb   # notebook da entrega
├── data/
│   └── tab_professores.txt   # professor, custo e disciplinas que já ministrou
└── .gitignore
```

## Execução

Abra o notebook a partir da raiz do repositório e execute **Restart Kernel → Run All**.

O arquivo de dados necessário está na pasta `data/` e é lido por caminho relativo. Os resultados são reprodutíveis porque cada execução do algoritmo genético fixa sua semente. A execução completa leva cerca de 1 a 2 minutos, pois o estudo de parâmetros roda o algoritmo 270 vezes.

## Tecnologias

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- SciPy
