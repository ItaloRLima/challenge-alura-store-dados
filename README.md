# Challenge Alura Store
Challenge feito para prática no curso de Ciência de Dados na plataforma da Alura. Tem como objetivo realizar uma análise de dados de 4 diferentes lojas de um mesmo dono e ao final redigir um relatório explicando qual deverá ser vendida e porque.<br>
O projeto foi feito utilizando as bibliotecas: 
- [Pandas](https://pandas.pydata.org/docs/) biblioteca feita para análise de dados;
- [Numpy](https://numpy.org/doc/) biblioteca feita para melhor trabalho com números e arrays;
- [Plotly](https://plotly.com/python/) biblioteca feita para demonstrar gráficos mais detalhados.
  
Através dessas bibliotecas fui capaz de fazer a análise dos dados e demonstrar os resultados através de gráficos bem apresentados.<br>

## Instruções de execução do código
1. Baixe o arquivo [AluraStoreBrasil](https://github.com/ItaloRLima/challenge-alura-store-dados/blob/main/AluraStoreBrasil.ipynb), ele virá na extensão .ipynb
2. Entre no site do [Google Colab](https://colab.google)
3. Acesse a opção Open Colab, no canto superior direito.
4. Vá para a opção "Upload" e arraste o arquivo para la.<br>
   <img width="50%" height="30%" alt="Captura de tela 2026-01-09 150140" src="https://github.com/user-attachments/assets/3d6898dc-0258-43e4-b0d8-cca8281ed234" />


## Conteúdo
### Extração dos dados
Para iniciar a análise dos dados foi necessário realizar a extração e transformação de dados em .csv para um dataframe. Para isso utilizamos a biblioteca Pandas.
<img width="1045" height="179" alt="image" src="https://github.com/user-attachments/assets/4e7440d8-4f2d-444f-a19e-d257fbb4f898" />
Com os dados em mãos, partimos para o que será levado em consideração pelo Senhor João.
### Faturamento
Após extração de dados utilizamos o método `loja['Preço'].sum()` onde pegamos a coluna "Preço" do dataframe e somamos todos os valores para no final obtermos o faturamento total daquela loja.<br>
<br><img width="587" height="416" alt="gráfico com o faturamento total de cada loja" src="https://github.com/user-attachments/assets/9364664b-5d75-4894-9310-fc349ffd5c4e" /><br>
Através dele podemos perceber que a loja 1 foi a que teve o maior faturamento dentre as outras. Enquanto a Loja 4 obteve o menor faturamento dentre todas, o que a torna uma opção para venda.

### Vendas por categoria
Utilizei o método `loja['Categoria do Produto']` que faz a contagem de valores únicos em linhas no dataframe para descobrirmos quanto de cada categoria foi vendido por loja.<br>
<br><img width="228" height="177" alt="image" src="https://github.com/user-attachments/assets/c0a3e030-102a-4a05-b36c-f864b5afe898" /><br>

Para melhor visualização, foram feitos quatro gráficos de pizza demonstrando a porcentagem da venda total de cada categoria em cada loja.<br>

<img width="70%" height="50%" alt="image" src="https://github.com/user-attachments/assets/c84ca9a7-1c1b-4fc8-871d-849ad0ab0afe" /><br>

Nas lojas de 1 a 3 ambas as categorias mais e menos vendidas foram Moveis e Utilidades domésticas, respectivamente.

### Média de avaliação das lojas
Utilizei o método `loja['Avaliação da compra'].mean()` que faz a média dos valores na coluna de Avaliação de compra.<br>
<br><img width="556" height="436" alt="image" src="https://github.com/user-attachments/assets/79596272-7919-48b2-8daf-d6ea237c3721" /><br>

Conseguimos ver que, embora apresente o maior faturamento entre as lojas a Loja 1 apresenta menor média de satisfação entre os clientes.

### Preço médio do frete por loja
Semelhante ao tópico anterior utilizei o método `loja['Frete'].mean()` que faz a média dos valores da coluna Frete.<br>
<br><img width="543" height="436" alt="image" src="https://github.com/user-attachments/assets/104920eb-209e-4de5-a990-ee3888f0c661" /><br>

A loja que tem o frete mais barato é a loja 4.

### Resultado Final
Com base na análise integrada dos dados, recomenda-se que o Senhor João opte pela venda da Loja 4.

Justificativa: A Loja 4 apresenta a pior performance financeira do grupo, faturando cerca de 10% a menos que a líder. O ponto mais crítico para essa decisão é a ineficiência de sua vantagem logística: ela possui o frete mais barato de todas, mas falha em transformar esse benefício em volume de vendas.

Enquanto a Loja 1 garante o caixa (apesar da baixa nota, que pode ser corrigida com gestão) e a Loja 3 garante a reputação da marca (melhor nota), a Loja 4 não lidera em nenhum pilar estratégico (nem financeiro, nem de qualidade), tornando-se a unidade mais dispensável para o grupo neste momento.
