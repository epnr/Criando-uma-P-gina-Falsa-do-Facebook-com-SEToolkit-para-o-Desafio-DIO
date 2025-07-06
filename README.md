# Criando-uma-P-gina-Falsa-do-Facebook-com-SEToolkit-para-o-Desafio-DIO
Criando uma Página Falsa do Facebook com SEToolkit para o Desafio DIO
Criar a página falsa do Facebook usando o SEToolkit para o meu desafio da DIO. Este é um exercício educacional e deve ser realizado em um ambiente controlado, como uma máquina virtual (VM), e nunca para fins maliciosos.

Ferramentas Necessárias

    Kali Linux (Recomendado): É a distribuição Linux mais popular para testes de penetração e já vem com o SEToolkit pré-instalado. Você pode rodá-la em uma máquina virtual (VirtualBox, VMware).

    SEToolkit (Social-Engineer Toolkit): A ferramenta que usaremos para gerar a página falsa.

    Conexão com a internet.

Passo a Passo: Configurando o SEToolkit

    Abra o Terminal no Kali Linux:
    No Kali Linux, clique no ícone do terminal (geralmente um quadrado preto ou uma janela de comando).

    Inicie o SEToolkit:
    Digite o seguinte comando e pressione Enter:
    Bash

    sudo setoolkit

    Você pode precisar digitar sua senha de usuário.

    Aceite os Termos e Condições:
    Na primeira vez que você roda o SEToolkit, ele pode pedir para aceitar os termos de serviço. Digite "y" para aceitar.

    Selecione a Opção de Ataque de Engenharia Social:
    No menu principal do SEToolkit, digite 1 (Social-Engineering Attacks) e pressione Enter.

    Selecione a Opção de Ataque de Website:
    No próximo menu, digite 2 (Website Attack Vectors) e pressione Enter.

    Selecione a Opção de Credential Harvester Attack Method:
    Agora, digite 3 (Credential Harvester Attack Method) e pressione Enter. Esta opção é projetada para capturar credenciais.

    Selecione a Opção de Clone Site:
    Você verá algumas opções. Digite 2 (Site Cloner) e pressione Enter. Esta opção permite clonar um site existente.

    Obtenha o IP Local para o Ataque:
    O SEToolkit perguntará se você quer usar o IP de um NAT/Port Forwarding. Para testes locais, você geralmente pode usar o IP local da sua máquina Kali. O SEToolkit pode até sugerir um. Se você precisar de um túnel para a internet (para que a página seja acessível de fora da sua rede), você usaria ferramentas como Ngrok ou Serveo, mas para o desafio e testes iniciais, o IP local basta. Digite o número correspondente à sua interface de rede ou apenas pressione Enter se ele sugerir o correto.

    Insira a URL para Clonar:
    Aqui está a parte crucial: você precisa da URL exata da página de login do Facebook. Geralmente, é https://www.facebook.com/. Digite esta URL e pressione Enter.

    Enter the full URL of the site you want to clone: https://www.facebook.com/

    Aguarde o SEToolkit Fazer seu Trabalho:
    O SEToolkit agora vai clonar a página do Facebook e configurar um servidor web simples para hospedar a página falsa. Ele também configurará um "Credential Harvester" para capturar os dados digitados na página.

    Localize a Página Falsa e o Arquivo de Log:

        Página Falsa: O SEToolkit indicará o IP e a porta onde a página falsa está sendo executada (ex: http://seu_IP_aqui:80). Você pode abrir um navegador na sua máquina host (ou em outra VM na mesma rede) e digitar este endereço para acessar a página falsa.

        Arquivo de Log: As credenciais capturadas serão salvas em um arquivo de log. O SEToolkit geralmente informa o caminho do arquivo, que costuma ser algo como /var/www/html/harvester_credentials.txt ou similar, dependendo da sua versão e configuração. Fique de olho na saída do terminal do SEToolkit.

    Testando a Captura:

        No navegador, acesse o endereço da página falsa (http://seu_IP_aqui:80).

        Digite um email e uma senha (falsos, claro!) na página.

        Pressione "Entrar". O SEToolkit tentará redirecionar a vítima para a página real do Facebook (o que ajuda a enganar a vítima).

        Volte ao terminal onde o SEToolkit está rodando. Você deverá ver as credenciais capturadas exibidas na tela e também salvas no arquivo de log.

O Que Documentar no seu README.md no GitHub

Lembre-se que a parte mais importante para o desafio da DIO é a documentação. No seu README.md, você deve explicar:

    Objetivo: Criar uma página de login falsa do Facebook para demonstrar a captura de credenciais usando SEToolkit.

    Ferramentas: Kali Linux, SEToolkit.

    Passos Realizados: Detalhe cada um dos passos que descrevi acima. Use screenshots (capturas de tela) do SEToolkit em cada etapa relevante, colocando-as na pasta /images.

    Resultados: Mostre uma captura de tela da página falsa no navegador e outra do terminal do SEToolkit exibindo as credenciais capturadas.

    Considerações Éticas: Reforce que este projeto é apenas para fins educacionais e que o uso dessas técnicas para atividades maliciosas é ilegal e antiético.
