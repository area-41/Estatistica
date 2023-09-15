# Exemplos de uso de Intervalo de Confiança sem Sigma

### Oxigênio na água
![image](https://github.com/area-41/Estatistica/assets/87396846/f1c4a54b-9c88-4513-b7bd-7aa07186d32a)

### Para calcular o intervalo de confiança para a média de oxigênio em um lago, sem conhecer o desvio padrão populacional (σ), Dionatam pode usar um intervalo de confiança baseado na distribuição t de Student, com o programa R, que possui funções específicas para isso. Com uma amostra de 30 medições de níveis de oxigênio em ppm (partes por milhão) do lago, pode calcular um intervalo de confiança de 95%.

#### Defina seus dados (amostra de medições de oxigênio)
    amostra <- c(8.2, 7.8, 8.0, 8.5, 7.7, 8.3, 7.9, 8.1, 8.4, 8.2, 7.6, 8.2, 7.9, 8.0, 8.3, 8.1, 8.6, 8.2, 7.8, 8.4, 8.0, 8.1, 7.7, 8.5, 7.8, 8.3, 8.2, 8.4, 7.9)

#### Calcule a média e o desvio padrão da amostra
    media_amostra <- mean(amostra)
    desvio_padrao_amostra <- sd(amostra)

#### Calcule o erro padrão da média (SE)
    erro_padrao_media <- desvio_padrao_amostra / sqrt(length(amostra))

#### Calcule o intervalo de confiança de 95%
    intervalo_confianca <- qt(c(0.025, 0.975), df = length(amostra) - 1) * erro_padrao_media + media_amostra

#### Calcule a média do intervalo
    t.test(amostra, conf.level=0.95)

#### Exiba o intervalo de confiança
    cat("Intervalo de Confiança (95%): [", intervalo_confianca[1], ", ", intervalo_confianca[2], "]\n")

Intervalo de Confiança (95%): [ 8.005271 ,  8.208522 ]

A 'amostra' representa os dados das medições de oxigênio. A função 'mean' calcula a média da amostra e 'sd' calcula o desvio padrão amostral. 
O 'erro padrão' (SESE) é calculado como o desvio padrão da amostra dividido pela raiz quadrada do tamanho da amostra.

A função 'qt' é usada para encontrar os valores críticos da distribuição t de Student, com base no nível de confiança desejado. 
Em um intervalo de confiança de 95%, usa-se os percentis 2.5% e 97.5%.


![image](https://github.com/area-41/Estatistica/assets/87396846/60f4b01b-d544-4532-b527-42b18e1ffedc)

----
## Tempo de Execução do Software

![image](https://github.com/area-41/Estatistica/assets/87396846/20f87367-6169-4c1f-b237-9c5f572fb40f)

### Uma empresa de engenharia de software está desenvolvendo um novo sistema para executar um programa e precisa determinar o tempo médio necessário para a sua realização. Para os testes executou esse programa por 20 vezes obtendo um tempo médio de 352 segundos e um desvio padrão de 8 segundos. Para um intervalo de 99% de confiança, calcular o verdadeiro tempo médio para execução desse programa.

Parâmetro: Tempo médio para execução desse programa (em segundos).
- σ NÃO é conhecido
- Tabela t-Student
- Dados resumidos: n=20; 𝑥ҧ=352 ; s=8

#### Intervalo de confiança para uma média -> Sigma NÃO é conhecido
#### Fornecer os dados do problema 
    n <- 20
    xbar <- 352 
    s <- 8
    NC<-0.99
    p<-NC+((1-NC)/2)

#### valor critico
    t<- qt(p, n-1, lower.tail = TRUE, log.p = FALSE) 
#### margem de erro
    erro <- t*s/sqrt(n) 
#### limite inferior do intervalo
    li <- xbar-erro 
#### limite superior do intervalo
    ls <- xbar+erro
#### impressão dos resultados
#### Valor crítico (t)
    print(t)
#### Margem de erro do intervalo de confiança calculado (E)
    print(erro)
#### Intervalo de confiança [li ; ls]
    print(li)
    print(ls)
    cat("Intervalo de Confiança (99%): [", li, ", ", ls, "]\n")

![image](https://github.com/area-41/Estatistica/assets/87396846/32dfb69d-5890-43fe-b4f4-a871c6bd72d5)



