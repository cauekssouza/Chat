Os Sockets Foram utilizados para criar uma conexão entre o servidor e cliente, fazendo com que
permitisse a transferência de dados com por exemplo inserir o nome e depois conversar
normalmente com servidor. O código utiliza a biblioteca socket para criar e gerenciar a conexão
entre os clientes e o servidor. No arquivo cliente.py, a função recebeDados é responsável por
receber mensagens do servidor e exibir em um terminal. A função utiliza o método recv() para
receber mensagens do servidor e imprime cada mensagem recebida. No server.py, a
função recebeDados é responsável por receber mensagens do cliente e realizar o broadcast para
todos os clientes conectados. A função utiliza o método recv() para receber mensagens do
cliente e imprime cada mensagem recebida. Já threads são usadas para lidar com a comunicação
com cada cliente de forma independente. No server.py, para cada nova conexão de cliente
aceita, uma nova thread é iniciada com o comando threadCliente =
threading.Thread(target=recebeDados, args=[conn, ender]) threadCliente.start(). O tratamento
broadcast no servidor é feito através da função broadcast, que envia a mensagem para todos os
clientes conectados, exceto o cliente de origem. Essa função é chamada na
função recebeDados do servidor, permitindo que o servidor envie a mensagem atualizada para
todos os clientes. No cliente, a função recebeDados é responsável por receber mensagens do
servidor e exibir em um terminal. A função utiliza o método recv() para receber mensagens do
servidor e imprime cada mensagem recebida.


Requisitos:
RF-01: O servidor deve ser capaz de lidar com múltiplos clientes simultaneamente.

RF-02: O chat deve ser capaz de lidar com desconexões de cliente, informando os outros
usuários conectados ao chat quando um usuário se desconectar.

RF-03: Ao entrar no chat, o usuário deve ser solicitado a escolher um nome de usuário.

RF-04: Se um usuário digitar ‘sair’, o chat deve encerrar a conexão desse usuário e informar os
outros usuários que ele saiu do chat.

RF-05: Quando um usuário envia uma mensagem, essa mensagem deve ser exibida no console
do usuário. Permitindo que o usuário veja o que ele enviou.

RF-06: Quando um novo usuário se conecta ao chat, uma notificação deve ser enviada a todos
os usuários já conectados informando que um novo usuário entrou no chat.

RF-07: Cada mensagem enviada deve ser precedida pelo nome do usuário que a enviou. Isso
permite que os outros usuários vejam quem enviou cada mensagem.
