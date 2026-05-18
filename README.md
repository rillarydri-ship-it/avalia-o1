# avalia-o1
avaliação 18/05/2026
Rillary Franco Rodrigues


Algoritmo "ENERGIA_ELETRICA"

Var
   consumo, geracao, bandeira, consumoliquido: real
   tarifa, taxafixa: real
   valorenergia, valorbandeira, valorfinal: real
   credito: real
   adicionalbandeira: real
   blocos100:inteiro

Inicio
   escreval("Digite o consumo mensal (kWh):")
   leia(consumo)
   escreval("Digite geracao solar(kWh):")
   leia(geracao)
   escreval("Digite o valor tarifa (r$/kWh):")
   leia(tarifa)
   escreval("Digite a taxa fixa minima (R$):")
   leia(taxafixa)
   escreval("Digite bandeira tarifaria")
   leia(bandeira)
   escreval("_____________________________________")
   escreval("0 - verde")
   escreval("1 - amarela")
   escreval("2 - vermelhapatamar1")
   escreval("3 - vermelhapatamar2")
   escreval("Opção: ")
   leia(bandeira)

   se bandeira = 1 entao
      adicionalBandeira <- 1,885
   senao
      se bandeira = 2 entao
         adicionalBandeira <- 4.463
      senao
         se bandeira = 3 entao
            adicionalBandeira <- 7.877
         senao
            adicionalBandeira <- 0
         fimse
      fimse
   fimse

   consumoliquido <- consumo - geracao

  se consumoliquido > 0 entao
  blocos100 <- int(consumoliquido/100)
   valorEnergia <- consumoLiquido * tarifa
    valorBandeira <- blocos100 * adicionalBandeira
    credito <- 0
    valorFinal <- valorEnergia + valorBandeira + taxaFixa
  senao
    blocos100 <- 0
    valorEnergia <- 0
    valorBandeira <- 0
    credito <- consumoLiquido * (-1)
    valorFinal <- taxaFixa
  fimse
    escreval("____________________________")
  escreval("Consumo Líquido: ", consumoLiquido:0:2, " kWh")
  escreval("Blocos de 100 kWh cobrados: ", blocos100)
  escreval("Credito Gerado: ", credito:0:2, " kWh")
  escreval("Valor da bandeira: R$ ", valorBandeira:0:2)
  escreval("Valor final da conta: R$ ", valorFinal:0:2)
Fimalgoritmo


