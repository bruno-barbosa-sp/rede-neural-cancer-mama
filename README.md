# Rede neural para classificação de tumores

Projeto da disciplina **Matemática para Ciência de Dados**, desenvolvido por **Bruno Aparecido Barbosa**.

O projeto adapta o arquivo `exemplo4.py` para a base Breast Cancer Wisconsin, disponível no `scikit-learn`.

A rede foi implementada com Keras e possui duas camadas ocultas:

```text
30 atributos -> 16 neurônios (ReLU) -> 8 neurônios (ReLU) -> 1 neurônio (sigmoide)
```

Foram preparadas duas versões da mesma rede. A primeira usa Keras e o otimizador Adam. A segunda implementa manualmente, com NumPy, a propagação para frente, a retropropagação e a atualização dos pesos por descida do gradiente. As duas usam entropia cruzada binária e mini-batches de 16 amostras.

## Como executar no VS Code

1. Abra esta pasta no VS Code.
2. Crie um ambiente virtual:

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

3. Instale as dependências:

   ```powershell
   python -m pip install --upgrade pip
   python -m pip install -r requirements.txt
   ```

4. Abra `relatorio_rede_neural.ipynb` para a versão em Keras ou `relatorio_rede_manual.ipynb` para acompanhar os cálculos implementados manualmente.
5. Selecione o interpretador da pasta `.venv` como kernel.
6. Use **Run All** para executar todas as células.

O notebook configura o Keras para usar o PyTorch como backend. A base de dados é carregada diretamente pelo `scikit-learn`; não é necessário baixar um arquivo separado.

## Arquivos

- `relatorio_rede_neural.ipynb`: relatório e implementação com Keras;
- `relatorio_rede_manual.ipynb`: relatório da implementação manual com NumPy;
- `arquitetura_rede.png`: diagrama da arquitetura;
- `historico_treinamento.png`: curvas de perda e acurácia;
- `matriz_confusao.png`: matriz de confusão no conjunto de teste;
- `fluxo_rede_manual.png`: fluxo detalhado da propagação e da retropropagação;
- `historico_rede_manual.png`: curvas da implementação manual;
- `matriz_confusao_manual.png`: matriz de confusão da implementação manual;
- `requirements.txt`: dependências necessárias para reprodução.
