# Projeto Terapia XP | Roadmap do MPV

`Agentes na experiência`
|*S*|Terapeuta|Visitante|Servidor|
|-|-|-|-
|*s*|Ccapaz de alterar e ativar a experiência, alguém na posição de terapeuta que vai conversar com, escutar e apoiar Visitantes.|Pessoa que deve atravessar a experiência interagindo com objetos até atingir uma meta e, enquanto isso, relatar seu progresso para Terapeuta.|Mediador que permite a Terapeutas abrir salas e enviar códigos de convite para salas.|

`Controles para Visitantes na experiência 3D`
|*S*|Movimento|Mira|Interagir|
|-|-|-|-
|*s*|Toque na tela sem objetos, fazendo a câmera se movimentar|Mover o celular, ativando o giroscópio e girando a câmera|Toque na tela com objeto no centro da tela, fazendo o objeto responder|

# Descrição

App para terapia de exposição em VR que usa o celular como headset, onde Terapeuta e Visitante compartilham uma experiência onde Visitantes devem se sentir acompanhados para enfrentar fobias e situações que são manipuladas por Terapeutas. Enquanto na experiência, Visitantes e Terapeutas podem se escutar e conversar através dos telefones.

## MPV e estrutura básica
Para um MPV, foi decidida a experiência "Fobia por Cachorros" com: Cenário em grade, cenário simples, foto de um cachorro e 3D de um cachorro, ambos capazes de emitir som.

`Deve ser possível, para Pessoas:`
Entrar no mundo, olhar ao redor, andar para a frente ao tocar na tela do celular. Mandar e receber voz para Terapeuta. Ao se aproximar o suficiente da abstração do cachorro, poder, ao olhar diretamente para ela no centro da tela, interagir para receber reforço positivo.

`Deve ser possível, para Terapeutas:`
Saber que uma pessoa entrou no mundo e observar o que esta Pessoa está vendo no mundo. Mandar e receber voz para Pessoa. Mudar o cenário atual do mundo. Colocar a abstração de cachorro no cenário. Poder fazer a abstração latir, com opção de latido leve e latido forte. Poder colocar uma parede no mundo entre o ponto de nascimento da pessoa e o cachorro.

`Deve ser possível, para Servidor:`
Ter espaço para uma sala que pode ser criada pelo app Terapeuta. Emitir um código para Terapeuta que pode ser usado por Pessoa para se conectar diretamente à sala.

>No futuro, consideramos modelar o ambiente da sala com mais liberdade, como posicionar vários objetos em locais escolhidos a dedo pelos Terapeutas. Estes podem mudar a visão do próprio app entre "Visitante" e "Ambiente", onde Visitante mostra a visão no app de Visitantes, e Ambiente a visão de topo do ambiente, com controles para se aproximar ou se distanciar do cenário, mover a câmera, escolher um objeto e posicionar este livremente (exceto se este for interativo e entrar no raio de outro objeto interativo) e então poder ativar objetos com um toque ou modificar com um toque longo. Mesmo em avanços futuros, a meta é manter a infraestrutura mais econômica possível, para que, mesmo podendo ser utilizada ou melhorada por equipamentos mais avançados, mantenha o foco em terapias de baixo custo com tecnologia moderna.

### Método terapêutico:
— Definir nível de abstração ideal.

Ex.: Ter abstrações de um cachorro que vão de uma bola com textura ou uma imagem quadrada de um cachorro que pode latir a um modelo 3D que, além de latir, se movimenta.

— Estimular aproximação.

Ex.: Perguntar para a pessoa Visitante se pode procurar o cachorro, enquanto este late, ou fica parado esperando a Visitante notar onde ele está, ou dizer para a Visitante onde o cachorro está e perguntar se pode se aproximar dele, enquanto encoraja verbalmente (pela chamada), ou visualmente (ativando objetos no cenário), ou audivelmente (por sons na experiência) cada aumento de proximidade.

— Estimular contato.

Ex.: Quando a pessoa chegar perto o suficiente do cachorro, a tela mostra um ícone que funciona como um sinal de que ele é interagível. Terapeuta estimula Visitante a interagir com o cachorro, o que inclui estar olhando diretamente para ele, reconhecer o símbolo na tela e usar um botão no headset para chamar o cachorro. Nesse momento, o cachorro se aproxima.

— Se ocorrer contato, reforço positivo.

Ex.: Após cachorro se aproximar, faz alguma animação que indica o animal estar feliz e tranquilo, como sons agradáveis de cachorro e ele ficar parado no pé da pessoa, ou brincando. Outros estímulos como os descritos em Estimular aproximação também podem ser usados.


## Metas mecânicas
### Servidor
- [ ] Poder manter registros de Terapeutas com login e senha.
- [ ] Ter um espaço para inserir salas.
- [ ] Criar uma sala.
- [ ] Criar um código de convite que pode ser mostrado para Terapeutas.
- [ ] Permitir que Visitantes possam inserir um código de convite para entrar em uma sala.
- [ ] Ter uma biblioteca de objetos que podem ser posicionados no ambiente de uma sala, nesse caso uma bola com textura, uma foto 2D ou um modelo 3D de um cachorro.
### App para Terapeutas
- [ ] Poder entrar no servidor ao abrir o app.
- [ ] Poder criar uma sala ao entrar no servidor.
- [ ] Ter uma janela no topo com visão da câmera do app Visitante. Se não houver uma pessoa conectada, a janela ainda existe, mas com um sinal de "Sem conexão".
- [ ] Tem um menu para escolher se vai colocar um dos objetos da biblioteca do servidor.
- [ ] Tem um botão que faz o objeto inserido ter uma interação passiva, nesse caso latir.
- [ ] Poder conversar por voz através do App com Visitantes.
### App para Visitantes
- [ ] Poder inserir um código de convite e se conectar à sala.
- [ ] Movimentação através de toque em qualquer área da tela.
- [ ] Poder interagir com objeto interagível se estiver dentro de um raio x do objeto e com o objeto no centro da câmera.
- [ ] Poder conversar por voz através do App com Terapeutas.

Com isso, temos a funcionalidade mais básica possível de ambos os aplicativos.
