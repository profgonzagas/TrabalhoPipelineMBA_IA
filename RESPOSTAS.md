# Respostas do Trabalho - Pipeline de ML

## Identificação do Grupo

- **Integrantes:**
  1. Nome: Wellington Alves Gonzaga
  2. Nome:
  3. Nome:
  4. Nome:

---

## Parte 1: Resultados do Pipeline

### 1.1 O pipeline executou sem erros?
<!-- Marque com X a opção correta -->
- [ x] Sim
- [ ] Não

### 1.2 F1-Score obtido:
<!-- Copie o valor exibido ao final da execução -->
```
F1-Score: _0.4043______
```

### 1.3 Cole aqui o output final do pipeline:
<!-- Execute: python main.py e copie a saída -->
```

🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀
INICIANDO PIPELINE DE ML
🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀🚀


[ETAPA 1/4] Carregando dados...
==================================================
EXPLORAÇÃO DOS DADOS
==================================================
Shape: (5000, 8)
cliente_id              int64
idade                   int64
renda_mensal          float64
tempo_conta_meses       int64
num_produtos            int64
tem_cartao_credito      int64
score_credito         float64
respondeu_campanha      int64
dtype: object
   cliente_id  idade  renda_mensal  tempo_conta_meses  num_produtos  tem_cartao_credito  score_credito  respondeu_campanha
0           1     56      46917.46                229             4                   1          600.0                   1
1           2     69      41274.41                  9             3                   0          758.2                   0
2           3     46      40649.98                 25             2                   1          595.7                   1
3           4     32      44336.79                217             5                   1          584.3                   0
4           5     60      35301.68                225             4                   0          797.8                   0
==================================================

DISTRIBUIÇÃO DO TARGET
------------------------------
respondeu_campanha
0    2803
1    2197
Name: count, dtype: int64
respondeu_campanha
0    0.5606
1    0.4394
Name: proportion, dtype: float64
------------------------------

[ETAPA 2/4] Validando dados...
Validando dados...
✅ Dados válidos!

[ETAPA 3/4] Treinando modelo...
Dados de treino: 4000 registros
Dados de teste: 1000 registros
Treinando modelo...
✅ Modelo treinado!
Modelo salvo em: models/modelo_campanha.pkl

[ETAPA 4/4] Avaliando modelo...

==================================================
RESULTADOS DA AVALIAÇÃO
==================================================

📊 MÉTRICAS:
   Accuracy:  0.5550 (55.50%)
   Precision: 0.4951
   Recall:    0.3416
   F1-Score:  0.4043

📋 MATRIZ DE CONFUSÃO:
   Verdadeiros Negativos (TN): 404
   Falsos Positivos (FP):      154
   Falsos Negativos (FN):      291
   Verdadeiros Positivos (TP): 151

==================================================
🎯 F1-SCORE FINAL: 0.4043
==================================================

✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅
PIPELINE CONCLUÍDO COM SUCESSO!
✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅✅

📝 Anote o F1-Score no arquivo RESPOSTAS.md: 0.4043

```

---

## Parte 2: Interpretação dos Resultados

### 2.1 O modelo é bom ou ruim? Por quê?
<!-- Considere: F1 de 0.5 seria jogar moeda. Acima de 0.5 = melhor que aleatório. -->
O modelo é ruim, pois ficou com F1 abaixo de 0.5


### 2.2 O dataset é balanceado ou desbalanceado? Como você descobriu?
<!-- Dica: veja a proporção da variável target na exploração dos dados -->
Balanceado, pois a diferença é pequena.
respondeu_campanha
0    2803
1    2197


### 2.3 Por que usamos F1-Score e não apenas Accuracy neste caso?
<!-- Dica: pense no que aconteceria se o modelo previsse sempre 0 -->



---

## Parte 3: Validação de Dados

### 3.1 Liste as validações Pandera que você implementou:
<!-- Descreva cada validação que você adicionou -->

1. cliente_id: Tipo inteiro, notNull, unique
2. idade: entre 18 e 80
3. renda_mensal: entre 1000 e 50000
4. score_credito: entre 300 e 850
5. respondeu_campanha:Tipo inteiro, valore 0 ou 1

### 3.2 Por que validar dados ANTES de treinar o modelo?
<!-- Pense no contexto de produção: o que aconteceria se dados inválidos entrassem no modelo? -->
Economia de recurso, pois não ocorre gosto de tempo e processamento desnecessário


---

## Parte 4: Versionamento

### 4.1 Liste os commits que vocês fizeram (copie do git log):
<!-- Execute: git log --oneline e cole aqui -->
```
(cole o output do git log aqui)
```

### 4.2 Por que mensagens de commit descritivas são importantes?
<!-- Pense: se outra pessoa olhar o histórico, vai entender o que foi feito? -->



---

## Parte 5: Reflexão (Opcional)

### 5.1 Qual foi a maior dificuldade do grupo?



### 5.2 O que vocês fariam diferente se fossem refazer?



---

**Data de entrega:** ___/___/______
