![Steel Temperature Prediction](assets/banner.svg)

[English](README.md) · **Português** · [Portfólio](https://github.com/joaovspereira)

# Steel Temperature Prediction

## Problema e objetivo

Prever a temperatura final do aço com dados do processo industrial.

## Resultados documentados

MAE de 5,533 °C, RMSE de 7,481 °C e R² de 0,773. Redução de 45,3% do MAE frente à média de referência.

## Método

Integração de cinco tabelas, limpeza por regras de domínio, engenharia de atributos, comparação de regressões, validação cruzada e análise de resíduos.

## Tecnologias

Python · pandas · NumPy · scikit-learn · LightGBM · Matplotlib · Seaborn

## Evidências e execução

- [Notebook completo](notebooks/steel_temperature_prediction.ipynb)
- [Arquivos de dados necessários](data/README.md)
- [Dependências](requirements.txt)
- [Instruções de instalação](README.md#run-locally)

## Escopo e limitações

Avaliação retrospectiva com divisão aleatória de lotes. Durações, contagens e totais do processo exigem revisão de disponibilidade para prever mais cedo. A seleção da frequência de materiais antecedeu a divisão dos dados. Não houve medição de economia de energia. As dependências não representam um ambiente histórico travado por versão.

Projeto educacional desenvolvido no Data Science Bootcamp da TripleTen. A revisão de publicação dos projetos, exceto a reexecução documentada do petróleo, verificou estrutura e sintaxe sem repetir o treinamento completo. Os datasets não são redistribuídos.

[João Vitor Pereira](https://github.com/joaovspereira) · [Contato](mailto:joaovitorsouza20pereira@gmail.com)
