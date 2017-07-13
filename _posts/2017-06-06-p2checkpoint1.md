---
layout: post
title: "AD1 2017.1, Problema 2 - Checkpoint 1"
date: "2017-06-06"
author: "Daniyel Rocha"
published: true
tags: [htmlwidgets, r]
#output: html_document
---




{% highlight text %}
## Error in library("DT"): there is no package called 'DT'
{% endhighlight %}

Utilizaremos uma base de dados extraída do site IMDB. Os dados coletados são referentes uma listagem de diversas séries e informações de seus episódios. A explicação das variáveis está [aqui](https://github.com/nazareno/imdb-series). Utilizaremos uma representação gráfica para mostrar nossos dados e tentaremos responder uma pergunta utilizando esse recurso visual.



##Questionamento

- O público geralmente considera o último episódio de uma série finalizada como sendo ruim?

Esse problema envolve selecionar todas as séries da nossa base de dados que já não são mais exibidas. Para isso, realizei uma rápida pesquisa e fiz a filtragem daquelas que vão nos atender para esse quesito. Foram selecionadas as séries encerradas: Breaking Bad, Dexter, Friends, How I Met Your Mother, Prison Break. Então temos a seguinte tabela, relativa a avaliação do último episódio de cada série - que pode ser ordenada, caso necessário.




{% highlight text %}
## Error in datatable(., colnames = c("Nome da Série", "Número do Último Episódio", : não foi possível encontrar a função "datatable"
{% endhighlight %}
**(Clique no título da coluna para ordenar)**  
  
Dessa forma, podemos realizar a comparação entre as séries analisadas e dizer qual delas o público considera ruim. Entretanto, dizer que os últimos episódios de uma série e, consequentemente, seu final é ruim com base somente no último episódio não é algo que representa muito bem uma visão sobre o período final de uma série.
Uma abordagem que pode nos fornecer uma maior representatividade sobre o final de uma série é escolher um cojunto de episódios, incluíndo o último episódio. Neste caso, iremos utilizar o conjunto dos 10 episódios finais para fazer a análise e observar um panorama geral. Por ainda ser um conjunto pequeno de dados, todas as faixas de valores devem ser consideradas na análise. Dessa forma conseguimos ter uma visão mais ampla dos valores e da distribuição dos mesmos ao longo do tempo.

![plot of chunk s](/figure/source/P2CP1/2017-06-06-p2checkpoint1/s-1.png)
**(Passe o mouse nos pontos para mais informações)**  
  
Para essa visualização, podemos observar que a avaliação do último episódio por si só não tem muita representatividade sobre o final de uma série. Isso se percebe pois algumas séries apresentaram episódios finais cuja avaliação variou muito na sua parte final, como por exemplo Breaking Bad, How I Met Your Mother e Dexter. Entretanto, entre essas três, notamos que o padrão de variação de cada uma foi distinto em relação a outra.  
Em Breaking Bad, podemos constatar que sua variabilidade acontece em uma faixa de valores distinta, entre 9 e 10, e isso indica que para o público seu final foi muito bom. Entretanto, verificamos que, tanto com How I Met Your Mother quanto Dexter, a inconstância foi maior e numa faixa de valores maior. Os dados das avaliaçãoes dessas duas séries nos indicam que o final de Dexter foi decepcionante, com alguns poucos episódios que parecem ter criado alguma ao telespectador, e How I Met Your Mother estava com boas avaliações, mas os últimos foram ruins e o último episódio pode ter frustrdo o público. A última observação nos mostra que algo parece ter acontecido e decepcionado os telespectadores, já que somente os dois últimos destoam da sequência final. Já Friends e Prision Break tiveram pouca variação na qualidade de seus episódios - apresentaram uma sequência de episódios com qualidade crescente, apesar de Prision Break mostrar alguma variação.
