# Estatística 
utilizando o programa R versão 4.3.1

### Calcular o Tamanho Amostral utilizando o R

      Dentro do R, clicar em ‘Pacotes’, ‘Instalar pacotes’. O R abrirá uma janela em que você deve 
      selecionar o país que fornecerá o repositório do pacote R, por exemplo ‘Brazil (PA)’,clique em 
      ‘Ok’. Selecione o nome do pacote que você quer instalar, ‘samplingbook’, e clique em ‘OK’. 
      Aguarde o processo de instalação do pacote. 
      É necessário carregar o pacote antes de utilizá-lo.
      Clique em ‘Pacotes’, selecione ‘Carregar pacote’, selecione o pacote que você acabou de 
      instalar e clique em ‘Ok’.

### Para calcular o TAMANHO AMOSTRAL para se estimar uma MÉDIA utilize a função 
    sample.size.mean(e, S, N = Inf, level = 0.95)

onde:
-  e representa a margem de erro
-  S representa o desvio padrão da população
-  N representa o tamanho da população. Utilize N=Inf quando o tamanho populacional é desconhecido
-  level representa o nível de confiança 
  
### Para calcular o TAMANHO AMOSTRAL para se estimar uma PROPORÇÃO utilize a função
    sample.size.prop(e, P = 0.5, N = Inf, level = 0.95)
    
onde:
-  e representa a margem de erro
-  P representa a proporção estimada (valor que pode variar de 0 a 1)
-  N representa o tamanho da população. Utilize N=Inf quando o tamanho populacional é desconhecido
-  level representa o nível de confiança
