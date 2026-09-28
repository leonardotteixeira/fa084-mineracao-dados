# FA084 — Mineração de Dados

Aluno: Leonardo Teixeira  
RA: 245602  
UNICAMP

## Entrega 1 — Algoritmo Genético

Montagem de uma grade semanal de disciplinas (segunda a sexta, uma disciplina por dia) com o menor custo possível, usando um algoritmo genético. A função de fitness soma o custo dos professores alocados e aplica as penalidades do enunciado:

- ×2 se o professor nunca ministrou a disciplina;
- ×1,5 se um professor se repete;
- ×5 se uma disciplina se repete.

O notebook implementa mutação, cruzamento e o algoritmo genético e demonstra o ótimo global do problema. Também executa a configuração oficial (população 60, elitismo 20%, mutação 10%, 500 gerações) e a compara com uma configuração proposta em 30 execuções com sementes fixas.

## Entrega 2 — Regressão

Regressão linear simples entre as leituras de um protótipo de sensor e as de um instrumento de referência. A análise considera R², MSE e RMSE e interpreta o erro residual segundo os padrões apresentados na Aula 7: ideal, variância não constante, não linearidade, outlier e não independência.

## Estrutura

```
fa084-mineracao-dados/
├── README.md
├── algoritmo_genetico_grade_disciplinas_entrega.ipynb   # Entrega 1
├── regressao_sensor_referencia_entrega.ipynb            # Entrega 2
├── data/
│   ├── tab_professores.txt      # professor, custo e disciplinas que já ministrou
│   └── sensor_e_referencia.csv  # leituras do instrumento de referência e do protótipo
└── .gitignore
```

## Execução

Abra cada notebook a partir da raiz do repositório e execute **Restart Kernel → Run All**.

Os dados necessários estão na pasta `data/` e são lidos por caminho relativo, então não há outra dependência externa. Os resultados do algoritmo genético são reprodutíveis porque cada execução fixa sua semente. O notebook do algoritmo genético leva cerca de 1 a 2 minutos, pois executa 270 rodadas no estudo de parâmetros.

## Tecnologias

- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- SciPy
