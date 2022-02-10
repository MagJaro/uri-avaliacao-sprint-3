# atividadeAvaliativaSprint3
Este repositório contém um arquivo json e um link de acesso para blip Chat como forma de entrega da atividade avaliativa referente a Sprint 3. 

Link para o BlipChat: https://magda-nilce-roman-jarozeski-qya0a.chat.blip.ai/?appKey=dGVzdGVwaXp6YXJpYTI6MzdhZTYyM2YtMmIxYS00NWU2LTk0YTctMzBlNGFiNDViMTdl

Breve explicação: O bot é em sua maior parte baseado em regras, basicamente o usuário passa pelo bloco de boas vindas que contém um script para comprimentar de acordo com a hora, esse script foi construído utilizando a variável calendar.hour e condições if, as condições precisaram ser adaptadas (adiantamento de três horas) para se enxaicar no padrão GMT. Na sequência aparecem as opções de pizzas salgadas OU doces, o sabor escolhido fica armazenado em uma variável. Após escolher a pizza, o fluxo segue para o bloco de bebidas, que segue o mesmo padrão dos blocos anteriores. Ao escolher (ou não) uma bebida, o usuário é direcionado para o bloco de localização, se escolher a opção de entrega em casa o sistema solicita o cep do usuário (validado por um regex) e entrega as informações referentes ao endereço do mesmo por meio de uma requisição HTTP, que busca as informações do cep numa API online. O próximo passo é a confirmação do pedido, que apenas informa qual pizza e qual bebida foi escolhida, e então o fluxo segue para o pagamento e o pedido é finalizado. O último bloco serve para receber algumas opções de entradas do usuário e para finalizar o atendimento. No bloco de reclamações foi criado um registro de eventos que usei para testar a opção de análise por meio de relatórios do blip e também estudar as intenções, para isso o bot foi integrado ao DialogFlow. 

Coisas que eu gostaria de ter feito mas preciso de mais estudo para fazer: permitir que o usuário escolha mais de uma opção de pizza, seja doce ou salgada, no bloco de confirmação do pedido fazer um script pra calcular o valor total do pedido, na opção de pagamento por pix solicitar um comprovante de pagamento e quem sabe permitir que o usuário transite "livremente" nas opções de produtos, podendo voltar atrás, caso queira mudar algo no pedido. 



