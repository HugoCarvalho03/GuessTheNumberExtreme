# GuessTheNumberExtreme
Participantes:

Hugo Jeliel Ludgerio Carvalho

Fernando Antônio Muniz Goiana Filho

Aqui está uma imagem que ilustra o estado atual do projeto:

![image](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/2e713c0c-e01e-4610-9f64-97bb4c82772b)


# Cronômetro
Ao clicar em 'configurar', um sinal é enviado para os cronômetros dos Jogadores 1 e 2. Esse sinal ativa ou desativa um flip-flop do tipo D, o qual fornece uma indicação de qual cronômetro está ativo, acendendo o LED '-' no jogo. Isso também possibilita a modificação dos cronômetros através das entradas USP, DSP, UMP e DMP.

Se o botão de iniciar for pressionado, o início aciona um flip-flop, iniciando a partida e ativando a saída 'running'. Esta partida não pode ser interrompida, a menos que seja resetada, cortando o sinal de configuração e impedindo a reconfiguração do cronômetro.

Crono:

O crono utiliza os circuitos cont_9 e cont_5 que são circuitos que contam de 9 a 0 (cont_9) e outro de 5 a 0(cont_5), e quando um está em 9 e muda para 0 ele manda um pulso de clock, do mesmo modo o de 5 a 0.

![cronometro](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/789e3cb1-504c-4c20-9d78-e9e4a3423636)

cont_9:

A cada pulso de clock enviado, o circuito Num_Regra_9 analisa as saídas de Q e gerencia as entradas dos flip-flops do tipo D, coordenando a lógica do sistema de forma precisa e eficaz. Essa operação é fundamental para o funcionamento adequado do sistema, garantindo sincronia e coerência entre os diferentes elementos do circuito.

![contregra9](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/0483de13-c130-4875-bdff-a03a7562d9b5)

cont_5:

A cada pulso de clock enviado, o circuito Num_Regra_5  avalia as saídas de Q e  regula as entradas dos flip-flops tipo D. Esta ação é crucial para manter a sincronia e a coesão no funcionamento do sistema, assegurando um desempenho confiável e consistente em todos os seus componentes.

![contregra5](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/a82c6850-9f41-48db-a229-5760dcc20ef7)

Num_Regra_9:

Além de supervisionar as saídas, o circuito também realiza uma verificação se o estado anterior era zero e o registra na memória. Portanto, se o estado atual atingir nove e o anterior era zero, um pulso de clock é enviado para efetuar a troca. Este processo é crucial para garantir o funcionamento preciso e oportuno do sistema.

![regra9](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/bb7ba46a-7856-4b3e-8fe7-d3ead8a90117)

Num_Regra_5:

O circuito não apenas monitora as saídas, mas também verifica se estava no estado 5 e o registra na memória. Assim, se o estado atual alcançar zero vindo de cinco, um pulso de clock é acionado para efetuar a transição. Este procedimento é essencial para assegurar a operação precisa e oportuna do sistema.

![regra5](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/606b31b6-9f50-45e3-81f5-18806eaab7aa)

# Jogo

Comparador: 

Quando um pulso de clock é acionado, duas caixas geram números aleatórios que, se necessário, são convertidos em seus equivalentes negativos. Em seguida, esses valores são somados e comparados com os números que o usuário inseriu, que também foram somados. Se o resultado for menor ou maior, apenas um desses valores é retornado. Em caso de igualdade, uma segunda comparação é realizada, desta vez usando apenas uma coordenada. Se o valor for igual, é indicado que o usuário acertou, pois isso significa que ele chutou as coordenadas exatas. Caso contrário, o indicador de acerto permanece apagado, o que significa que o jogador acertou apenas na soma dos números. Este processo garante um fluxo preciso e eficiente no sistema de jogo.

![comparador](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/15a59723-5578-45f1-b8d8-0e72192b1fcf)

Negativos:

Este componente foi projetado para representar números negativos. Quando o bit mais significativo está definido como ativo, todos os bits são invertidos e um bit é adicionado ao resultado, resultando no valor negativo correspondente. Essa abordagem eficaz garante uma representação precisa e coerente dos números negativos no sistema.

![negativos](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/88318d8d-00dd-4f81-8863-fe4d26341561)

Placar: 

Após a comparação, se um jogador acertar, os placares correspondentes serão incrementados de acordo com o jogador em ação. Esta dinâmica assegura que o placar seja atualizado de maneira precisa e justa, refletindo o desempenho de cada jogador no jogo.

![placar](https://github.com/HugoCarvalho03/GuessTheNumberExtreme/assets/118187319/e048b8da-b222-4bb3-bff3-076cb95c27a6)









