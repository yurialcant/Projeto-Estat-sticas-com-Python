# Projeto Estatísticas com Python
| 🪧 Vitrine.Dev |     |
| -------------  | --- |
| ✨ Nome        | Projeto Estatísticas com Python
| 🏷️ Tecnologias | Python, Pandas, matplotlib
| 🚀 URL         | https://github.com/yurialcant/Projeto-Estatisticas-com-Python
| 🤿 Desafio |https://cursos.alura.com.br/course/estatistica-distribuicoes-e-medidas

<h1 align ="center"> Estatísticas com Python I </h1>
<p align="center">
<img src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=GREEN&style=for-the-badge"/>
</p>
#vitrinedev

Este projeto foi desenvolvido durante o curso de Estatísticas com Python I, nossa intenção é aprender os conceitos fundamentais aplicados na estatística utilizada por um profissional de Ciência de Dados.

<h1> Conhecendo a Base de Dados</h1>
<h2> Dataset do projeto</h2>
A base de dados escolhida para esse projeto, foi o relatório do PNAD (Pesquisa Nacional por Amostra de Domicílios) de 2015, as variáveis utilizadas nesse projeto, foram a renda, idade, altura, UF, Sexo, Anos de Estudo e cor/raça. Importamos a nossa base de dados e ao abrir encontramos, a seguinte distribuição em nosso DataFrame.

![Captura de Tela (206)](https://user-images.githubusercontent.com/102321564/194418502-10bb4426-8c3a-41cb-8938-7b066946f040.png)

Seguimos para a análise dos tipos de dados, dividimos eles em Variáveis Qualitativas Ordinais (que podem ser ordenadas ou hierarquizardas), Variáveis Qualitativas nominais (que não podem ser ordenadas ou hierarquizardas), Variáveis Quantitativas Discretas (que representam uma contagem, onde os valores possíveis formam um conjunto finito ou enumerável), Variáveis Quantitativas Contínuas (que representam uma contagem ou mensuração, que assumem valores em uma escala contínua) e encontramos a seguinte distribuição.

![Captura de Tela (207)](https://user-images.githubusercontent.com/102321564/194419520-6f425053-fec1-4159-b3e8-5f6ba449f03d.png)
![Captura de Tela (208)](https://user-images.githubusercontent.com/102321564/194419584-ca2d1200-6052-4a31-9c80-9d293e8c5e61.png)

<h1> Distribuição de Frequências </h1>
<h2> Distribuição de Frequências para Variáveis Qualitativas</h2>
Nesta etapa, buscamos conhecer o comportamento das variáveis envolvidas no projeto, primeiro começamos pelas variáveis qualitativas e utilizamos 2 métodos. O primeiro método foi atribuir cada coluna das nossas variáveis qualitativas, para uma nova variável tanto da frenquência como do percentual e assim criar um DataFrame para cada variável.

![Captura de Tela (209)](https://user-images.githubusercontent.com/102321564/194420524-bd4c8e8f-e100-42db-90d1-47b7c7fa19b3.png)![Captura de Tela (210)](https://user-images.githubusercontent.com/102321564/194421021-3b2bcc66-63fc-4c9f-950b-5a3b138d1dae.png)

Nosso segundo método, se baseou em utilizar um método do pandas chamado crosstab, para criar um DataFrame que cruzasse as informações da cor com o sexo e depois criamos outro DataFrame com o mesmo método, mas dessa vez adicionando a aggfunc, para distribuir a média da Renda em nosso DataFrame.
![Captura de Tela (211)](https://user-images.githubusercontent.com/102321564/194421597-ed1805f4-9904-4f3a-9d7b-606862ccae05.png)![Captura de Tela (212)](https://user-images.githubusercontent.com/102321564/194421676-a982c0a9-ace8-47ed-8a35-5296bcec9e9c.png)


<h1> Distribuição de Frequências</h1>
<h2> Variáveis quantitativas</h2>
Agora iremos realizar a distribuição de frenquência para as variáveis quantitativas, o primeiro passo para realizar isso é especificar os limites de cada classe, neste exemplo iremos usar a renda, portanto dividimos a nossa classe com base nos limites de renda.


![Captura de Tela (213)](https://user-images.githubusercontent.com/102321564/194774825-5a3edbab-24bc-4f34-9ab7-ddc21fe543c2.png)

O segundo passo consiste em criar a tabela de frequência, para isso usaremos a função cut do pandas passando como parâmetros as classes e os labels que criamos, incluido o comando "include_lowest" para incluir na nossa tabela o número 0, então após criarmos as tabelas de frequência e de percentual, passaremos as duas para um novo Data Frame e depois usamos o parâmetro ascending como falso, para ordenar o nosso Data Frame.


![Captura de Tela (214)](https://user-images.githubusercontent.com/102321564/194775021-c5adec38-801b-429f-9719-34cb7eef5c19.png)


<h1> Distribuição de Frequências</h1>
<h2> Histograma</h2>

Nesta etapa, criaremos um histograma que é a representação gráfica de uma distribuição de frequências, para isso importaremos a biblioteca seaborn, onde através dela conseguiremos montar nosso histograma usando a função histplot e passando a coluna de nosso DataFrame que desejamos criar no histograma.

![Captura de Tela (215)](https://user-images.githubusercontent.com/102321564/194775233-b81c8809-bc0f-42f7-83f4-7ce7730be813.png)

Podemos criar a gráficos com a biblioteca pandas, mas perdemos algumas funções e nossos gráficos ficam mais simples, para criar um gráfico de barras, basta usar a função plot.bar e passar os parâmetros desejados no gráfico.

![Captura de Tela (216)](https://user-images.githubusercontent.com/102321564/194775319-53262e12-4fa0-4cfe-b2b3-3655a8c43cd1.png)

<h1> Medidas de Tendência Central </h1>
<h2> Relação entre média, mediana e moda</h2>
Nesta etapa, usaremos a biblioteca seaborn novamente, para avaliarmos as medias de tendência central e as funções mode, median e mean para obtermos as medidas de algumas variáveis, o resultado pode ser visto nas imagens abaixo.

![Captura de Tela (217)](https://user-images.githubusercontent.com/102321564/194775509-b32e79f2-cf18-4fd0-859a-71775a3f5307.png)

![Captura de Tela (218)](https://user-images.githubusercontent.com/102321564/194775540-d5913e42-b5a9-4245-b5d5-182c2903953c.png)

![Captura de Tela (219)](https://user-images.githubusercontent.com/102321564/194775579-59b79a12-b7af-4a71-b837-c5ea4beb57fe.png)

Podemos ver que as medidas, são extremamente bem representadas nos gráficos, nos dando uma visualização extremamente fiel aos resultados obtidos pelas funções mode median e mean.

