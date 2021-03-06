# Relógio Heckethorn
> Simulação do relógio de Julius Heckethorn, do romance Avalovara de Osman Lins.

## O Mecanismo
No romance Avalovara, um dos personagens, chamado Julius Heckethorn, produz um relógio que toca trechos da música "Sonata em Fá Menor K.462" de Scarlatti a cada hora, de forma aparentemente caótica, mas com um mecanismo lógico.

## A Música
A música de Scarlatti pode ser ouvida pelo link abaixo, na interpretação de Lucas Debargue. O trecho utilizado pelo personagem Heckethron em seu relógio são os primeiros 21 segundos, ou as primeiras 10 medidas da partitura. Esse trecho é dividido em 13 partes, as quais são tocadas numa frequência definida pelo mecanismo do relógio.

[Ouça no Spotify](https://open.spotify.com/track/4K8laOLYWtfW1NKszo7H4f?si=54ec24fb2022444f)

## Periodicidade
O que determina quais trechos irão tocar a cada hora não é o horário específico, e sim quantas horas se passaram desde a última vez que a música tocou por completo.

Grupo | Partes | Frequência
----- | ------ | ----------
A | 1, 5, 11 | 11 horas
B | 2, 4, 7, 9 | 13 horas
C | 3, 6, 8, 10, 13 | 21 horas
D | 12 | ~5 horas*

*O grupo D (parte 12) acrescenta um elemento aleatório ao mecanismo, ele pode tocar de 5 em 5 horas ou pode vir a atrasar ou adiantar.

Seguindo essa lógica, a cada 3003 horas (11 x 13 x 21 = 3003) a música vai tocar pelo menos 12 das 13 partes. O momento exato em que as 13 serão emitidas em ordem e a introdução da música será tocada por completo fica indefinido.

## A Simulação
A intenção do presente código é gerar uma simulação do relógico descrito no romance, de forma a facilitar o entendimento de como ele funciona e possibilitar a apreciação da ideia do autor através de um protótipo concreto.

## Versão Atual
**OBS: É necessário autorizar o navegador para liberar a reprodução de som! O padrão do navegador é bloquear.**

Atualmente temos duas páginas, uma com tempo acelerado e outra com tempo real, uma mostrando a lógica e o funcionamento do mescanismo de forma mais prática e a outra para apreciar o ritmo lento e aparentemente caótico com que a criação de Osman Lins se apresenta.

O código utiliza Next.js para o rápido deployment e atualização de incrementos através do Vercel. A interface tem apenas o relógio por enquanto, cujo código em React foi retirado [desse sandbox](https://codesandbox.io/s/idkpz?file=/src/Clock.js) de autoria de 'asimgiri'.

A música é utilizada apenas de forma temporária, e os cortes das 13 partes não estão ainda exatamente como descritas no romance.