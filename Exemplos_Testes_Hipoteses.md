# Exemplos de uso de Testes de Hipóteses

![image](https://github.com/area-41/Estatistica/assets/87396846/89e42024-585a-4bbb-bccb-84c88243e243)
### Dieta
### Um pesquisador afirma que uma determinada dieta pode proporcionar uma perda média de peso de 12 kg no período de acompanhamento.
Ele quer verificar se uma nova dieta é mais eficaz, ou seja, proporciona maior emagrecimento. </br>
Para isso, ele acompanhou um grupo de 17 pacientes que seguiu a nova dieta e, decorrido certo tempo,</br>
observou a perda de peso de cada paciente do grupo.</br></br> 
Os dados estão apresentados a seguir:</br>
12, 8, 15, 13, 10, 12, 14, 11, 12, 13, 15, 19, 15, 12, 13, 16, 15.

Utilizando um nível de 5% de significância, o que você pode concluir?

### σ NÃO é conhecido  ->  Distribuição t-Student  -> Dados brutos H0: μ<12 e Ha: μ>12


### Software usado *Studio R*

    peso<-c(12, 8, 15, 13, 10, 12, 14, 11, 12, 13, 15, 19, 15, 12, 13, 16, 15)
    t.test(peso, alternative=c("greater"), mu=12, conf.level=0.95)

![image](https://github.com/area-41/Estatistica/assets/87396846/53926764-6327-41a1-9809-16ed716a41cd)

Como interpretar o valor p? SE rejeitarmos H0, cometemos um erro de 0,03099 ou 3,099%.

### Podemos dizer, com um nível de 5% de significância, que a nova dieta é mais eficaz, ou seja, proporciona maior emagrecimento. 
</br></br>  

------------
</br></br> 
![image](https://github.com/area-41/Estatistica/assets/87396846/d956c8aa-e2ae-4085-811b-fa8544e78ed6)

### Companhia de Ônibus
### Uma companhia de serviços de ônibus intermunicipais planejou uma nova rota para servir vários locais situados entre duas cidades importantes. 
Um estudo preliminar afirma que a duração das viagens pode ser considerada uma variável aleatória com distribuição normal, com média igual a 300 minutos e desvio padrão 30 minutos. 

Uma amostra de dez viagens realizadas nessa nova rota apresentou média igual a 314 minutos.</br></br>  

Esse resultado comprova ou não o tempo médio determinado nos estudos preliminares? 
Considere α=0,1.

### σ é conhecido -> Distribuição Normal -> Dados resumidos n=10; 𝑥ҧ=314 ; σ=30 -> H0: μ = 300 e Ha: μ ≠ 300

### Software usado *Excel*

![image](https://github.com/area-41/Estatistica/assets/87396846/9606d14c-507d-44ea-8beb-92d902e04184)

Como interpretar o valor p?</br> 
SE rejeitarmos H0, cometemos um erro de 0,14 ou 14%.</br></br>  
Como concluir o teste?</br> 
### Podemos dizer, com um nível de 10% de significância, que a duração média das viagens na nova rota é igual a 300 minutos, ou seja, comprova os resultados nos estudos preliminares.
</br></br>  
-----
</br></br>  
![image](https://github.com/area-41/Estatistica/assets/87396846/c3feac5f-d614-4497-960b-b656d751cdb5)

### Fabricante de Pen Drive
### Um fabricante de pen drives garante que, no mínimo, 90% de seus produtos são perfeitos. 
Uma amostra de 200 unidades desse produto foi inspecionada e verificou que 30 delas eram defeituosas. </br></br>

Teste a afirmação do fabricante ao nível de significância de 2%. 
O que você pode concluir?</br></br>

-> Dados resumidos n=200; x=170; ^p=170/200=0,85 </br>
-> H0: p > 0,90 e Ha: p < 0,90 </br>
-> n.p0=200.0,9=180 e n.(1-p0)=200.0,9=20 </br>
-> Distribuição Normal</br></br>

### Software usado *Excel*
![image](https://github.com/area-41/Estatistica/assets/87396846/b374b2b5-8485-4f10-9368-e3804adb84a3)

Interpretação do valor p:</br>
SE rejeitarmos H0, cometemos um erro de 0,00921 ou 0,921%.</br></br>

Conclusão do teste:</br>
### Considerando um nível de 2% de significância, podemos dizer que a proporção de pen drives perfeitos NÃO é de no mínimo 90%, ou seja, não podemos concordar com a afirmação do fabricante.
</br></br>

### Software usado *Studio R*
Utilizando a função binom.test do R para a resolução desse exercício:

    binom.test(170, 200, p = 0.9, alternative = c("less"), conf.level = 0.98)

  ![image](https://github.com/area-41/Estatistica/assets/87396846/831f1b8a-54b1-4e62-9fe6-fb1a48e2de8a)
</br></br>  

Utilizando a função prop.test COM correção de continuidade de Yates:

    prop.test(170, 200, p = 0.9, alternative = c("less"), conf.level = 0.98, correct=TRUE)

![image](https://github.com/area-41/Estatistica/assets/87396846/6f045e79-2608-464b-a92f-b56c17beada7)
</br></br>

Utilizando a função prop.test SEM correção de continuidade de Yates (correct=FALSE):

    prop.test(170, 200, p = 0.9, alternative = c("less"), conf.level = 0.98, correct=FALSE) 

![image](https://github.com/area-41/Estatistica/assets/87396846/50f4b393-cacf-4624-ba96-971e2075ec07)


### Valores encontrados:
✓ Utilizando a distribuição Normal:
Valor p = 0,00921

✓ Utilizando a distribuição Binomial:
Valor p = 0,01633

✓ Utilizando a distribuição Qui-quadrado com a correção de Yates:
Valor p = 0,01257

✓ Utilizando a distribuição Qui-quadrado sem a correção de Yates:
Valor p = 0,009211
</br></br>


Grato à Profª Julienne Borges 
</br></br>
