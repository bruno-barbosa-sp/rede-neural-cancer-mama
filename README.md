# Rede neural para classificação de tumores

Projeto da disciplina **Matemática para Ciência de Dados**, desenvolvido por **Bruno Aparecido Barbosa**.

O notebook adapta o fluxo do arquivo `exemplo4.py` para a base Breast Cancer Wisconsin, disponível no `scikit-learn`. A rede foi implementada com Keras e possui duas camadas ocultas:

```text
30 atributos -> 16 neurônios (ReLU) -> 8 neurônios (ReLU) -> 1 neurônio (sigmoide)
```

O treinamento usa o otimizador Adam, entropia cruzada binária e mini-batches de 16 amostras. O notebook também apresenta a arquitetura da rede, as curvas de treinamento e a matriz de confusão.

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

4. Abra `relatorio_rede_neural.ipynb`.
5. Selecione o interpretador da pasta `.venv` como kernel.
6. Use **Run All** para executar todas as células.

O notebook configura o Keras para usar o PyTorch como backend. A base de dados é carregada diretamente pelo `scikit-learn`; não é necessário baixar um arquivo separado.

## Arquivos

- `relatorio_rede_neural.ipynb`: relatório e implementação completa;
- `arquitetura_rede.png`: diagrama da arquitetura, também gerado pelo notebook;
- `historico_treinamento.png`: curvas de perda e acurácia;
- `matriz_confusao.png`: matriz de confusão no conjunto de teste;
- `requirements.txt`: dependências necessárias para reprodução.

> Este projeto tem finalidade exclusivamente educacional. O modelo não deve ser usado para decisões médicas.

