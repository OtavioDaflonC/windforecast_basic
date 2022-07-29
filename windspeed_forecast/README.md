Assunções:

* Por causa da correlação encontrada entre o ângulo do vento e a velocidade relativa, assume-se 3 possibilidades:

 -Que a turbina aeólica não possui o sistema de calibração de direção para otimizar a performance em ângulos desfavoráveis.
 -Que a taxa de variação da direção do vento pode fazer a calibração da turbina demorar mais ou menos para se ajustar,
justificando as correlações com a velocidade.
 -Que essa correlação observada se deve ao relevo à volta da usina afetando a velocidade do vendo em direções específicas.



Considerações:
* Outras considerações constam no notebook.

* Apesar de o target ser da velocidade do vento a 10m, seria interessante ter dados da velocidade relativa do vento medido
pelo anemômetro da turbina aeólica.

* Modelo foi elaborado com base no método de Ridge de regressão, considerando que essa opção minimiza eventualidades de overfiting.

* As unidades dos dados permanecem como apresentadas: Direção angular em graus e velocidades em metro por segundo.

* Foi feito um split. Tanto o teste quanto o treino foram estraídos do mesmo dataset, sem usar o forecast.csv apesar de
ter havido uma preparação para este dataframe no início. Acredito que isso não se desvia do propósito do exercício,
que é prever com sucesso um volume de teste e otimizar o erro.

* A métrica de análise de qualidade do modelo de previsão foi o erro quadrático médio.

* Apesar de algumas ideias não terem dado certo para otimizar o modelo, eu defendo que a lógica básica da ideia.
Como por exemplo no caso de tentar transformar as direções em uma feature melhor correlacionada com a velocidade do vento.
Imagino que tenha dado errado apenas porque para implementar no código decidi arredondar os valores para inteiros, o que 
deve ter atrapalhado a correlação.

Resultado:
Obteve-se com êxito um modelo de previsão que foi capaz de prever o conjunto de teste com erro quadrático médio de 
1.816 aproximadamente.

