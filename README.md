#Projeto SA - Jogo Descubra a Palavra
##Curso

#Técnico em Desenvolvimento de Sistemas
#UC: Lógica de Programação

#Descrição do Projeto

Desenvolvimento de um jogo de adivinhação de palavras para web.
O objetivo é aplicar conceitos fundamentais de lógica de programação, manipulação de DOM e organização de código em um projeto real de desenvolvimento.

#O jogador deve descobrir uma palavra secreta tentando adivinhar as letras.

#1️⃣ Quantas tentativas o jogador terá?
O jogador terá 6 tentativas, poucas tentativas para forçar o pensamento lógico na adivinhação da palavra secreta.

#2️⃣ Como o jogo irá mostrar a palavra oculta?
A palavra oculta aparecerá em lacunas, por exemplo: "_ _ _ _ _".

#3️⃣ O que acontece quando o jogador acerta uma letra?
A letra aparece nas lacunas correspondentes e ele ganha pontos.

#4️⃣ O que acontece quando o jogador erra uma letra?
O jogador perde pontos, e os erros ficam marcados abaixo da pontuação.

#5️⃣ O que acontece quando todas as letras são descobertas?
O jogador ganha a partida.

#6️⃣ O que acontece quando as tentativas acabam?
O jogador perde o jogo.

##Perguntas reflexivas!

#1) Como organizamos nosso projeto?
O nosso projeto foi em quatro partes, a dupla decidiu dividir a organização da seguinte forma: Safira fez parte do HTML e README, logo a Ana ficou responsável com o CSS, JAVASCRIPT e terminar o HTML.  

#2) O que foi mais difícil no layout?
A parte em que tivemos mais dificuldade no layout foi conseguir encontrar a fonte pixel certa(font-family: 'Press Start 2P' cursive;) e que mais se encaixasse no jogo, outra parte difícil foi nas combinações de cores.

#3) Nossa interface está preparada para receber JavaScript? Por quê?
Sim, a interface está preparada para receber o JavaScript porque o HTML está conectado com o arquivo script.js e possui os elementos identificados por classes e IDs que podem ser manipulados pelo JavaScript através da manipulação de DOM. 

##Variáveis
Para que o jogo funcione corretamente, utilizamos algumas variáveis que ajudam a controlar a lógica do jogo e as informações mostradas na tela.

A variável palavraSecreta guarda a palavra que o jogador precisa descobrir durante a partida.

Já a palavraOculta armazena a palavra escondida, mostrando apenas lacunas (_ _ _). Conforme o jogador acerta as letras, essas lacunas vão sendo substituídas pelas letras corretas.

A variável tentativasRestantes controla quantas tentativas o jogador ainda possui antes de perder o jogo.

A letrasUsadas guarda todas as letras que o jogador já tentou, para evitar que a mesma letra seja usada várias vezes.

Também utilizamos a variável palavras, que é uma lista com várias palavras possíveis que o sistema pode escolher de forma aleatória para iniciar o jogo.

Além dessas, existem algumas variáveis que servem para ligar o JavaScript com os elementos da página HTML.

A variável palavraElemento representa o espaço na tela onde a palavra oculta aparece.

A variável input representa o campo onde o jogador digita a letra que deseja tentar.

A variável botaoTentar representa o botão que o jogador usa para confirmar a letra digitada.

A variável tentativasTexto mostra na tela quantas tentativas ainda restam.

A variável letrasUsadasTexto exibe as letras que já foram utilizadas pelo jogador.

Por fim, a variável botaoComecar representa o botão responsável por iniciar o jogo.

##fluxo do jogo
O funcionamento do jogo acontece em algumas etapas.

Primeiro, o jogador clica no botão “Começar Jogo” para iniciar a partida. Em seguida, o sistema escolhe uma palavra aleatória da lista de palavras disponíveis no jogo.

Depois que a palavra é escolhida, ela aparece na tela de forma escondida, representada por lacunas (_) que indicam a quantidade de letras da palavra.

O jogador então digita uma letra no campo de entrada e clica no botão “Tentar”.

Após isso, o sistema verifica se a letra digitada é válida e se ela já não foi utilizada anteriormente.

Se a letra estiver presente na palavra secreta, ela aparece nas posições corretas da palavra, revelando parte da resposta para o jogador.

Caso a letra não esteja na palavra, o jogador perde uma tentativa.

A cada tentativa, o sistema atualiza as informações na tela, mostrando a palavra com as letras descobertas, o número de tentativas restantes e as letras que já foram utilizadas.

Durante o jogo, o sistema também verifica se o jogador descobriu todas as letras da palavra, o que significa vitória, ou se as tentativas acabaram, o que significa derrota.

Ao final da partida, o jogo mostra uma mensagem informando se o jogador venceu ou perdeu.

##Pseudocódigo:
INÍCIO DO JOGO

Criar uma lista com várias palavras de animais

Criar as variáveis:
palavraSecreta
palavraOculta
tentativasRestantes
letrasUsadas

Quando o jogador clicar em "Começar Jogo":

    Escolher uma palavra aleatória da lista
    Guardar essa palavra em palavraSecreta

    Criar a palavraOculta usando "_" para cada letra da palavra

    Definir tentativasRestantes como 6
    Limpar a lista de letrasUsadas

    Mostrar a palavra oculta na tela
    Mostrar as tentativas restantes

Quando o jogador digitar uma letra e clicar em "Tentar":

    Ler a letra digitada
    Transformar a letra em maiúscula

    Se a letra estiver vazia ou não for válida
        parar a tentativa
    fim

    Se a letra já tiver sido usada
        mostrar aviso para o jogador
        parar a tentativa
    fim

    Adicionar a letra na lista de letrasUsadas

    Se a letra existir na palavraSecreta

        Para cada posição da palavra
            Se a letra for igual
                revelar a letra na palavraOculta
            fim
        fim

    Senão
        diminuir tentativasRestantes em 1
    fim

    Atualizar a tela com:
        palavra atualizada
        tentativas restantes
        letras usadas

    Verificar se o jogo terminou

        Se não existir mais "_" na palavra
            mostrar mensagem de vitória
            encerrar o jogo
        fim

        Se tentativasRestantes for igual a 0
            mostrar mensagem de derrota
            mostrar a palavra secreta
            encerrar o jogo
        fim

FIM DO JOGO