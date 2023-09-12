# Estatística
utilizando o programa R versão 4.3.1
</br></br>

## Com sigma  σ
### Cálculo de intervalo de confiança para uma média com σ CONHECIDO

#### Intervalo de confiança para uma média -> Sigma É conhecido
###### Fornecer os dados do problema
    n <- 25
    xbar <- 300 
    sigma <- 18.5
    NC<-0.95
    p<-NC+((1-NC)/2)
##### valor critico
    z<- qnorm(p, mean = 0, sd = 1, lower.tail = TRUE, log.p = FALSE)
##### margem de erro
    erro <- z*sigma/sqrt(n)
##### limite inferior do intervalo
    li <- xbar-erro
##### limite superior do intervalo
    ls <- xbar+erro
##### impressão dos resultados
##### Valor crítico (z)
    print(z)
##### Margem de erro do intervalo de confiança 
    calculado (E)
    print(erro)
##### Intervalo de confiança [li ; ls]
    print(li)
    print(ls

![image](https://github.com/area-41/Estatistica/assets/87396846/cb56e090-aacb-4140-ad26-e857c6f9b2b4)

</br></br>

## Sem sigma σ

### Cálculo de intervalo de confiança para uma média quando σ NÃO É conhecido

#### Intervalo de confiança para uma média -> Sigma NÃO é conhecido
##### Fornecer os dados do problema 
    n <- 25
    xbar <- 300 
    s <- 18.5
    NC<-0.95
    p<-NC+((1-NC)/2)
##### valor critico
    t<- qt(p, n-1, lower.tail = TRUE, log.p = FALSE) 
##### margem de erro
    erro <- t*s/sqrt(n) 
##### limite inferior do intervalo
    li <- xbar-erro 
##### limite superior do intervalo
    ls <- xbar+erro
#### impressão dos resultados
##### Valor crítico (t)
    print(t)
##### Margem de erro do intervalo de confiança calculado (E)
    print(erro)
##### Intervalo de confiança [li ; ls]
    print(li)
    print(ls)

![image](https://github.com/area-41/Estatistica/assets/87396846/fb3563fb-b3b1-4091-a13c-e78b681d49cc)


