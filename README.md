( função () {

    // Definir a nossa função responsável por estender o bot.
    função de  estender () {
        // Se o bot não foi carregado corretamente, tente novamente em 1 segundo (s).
        se ( ! janela .bot) {
            retornar  setTimeout (estender, 1  *  1000 );
        }

        // As precauções para se certificar de que é atribuído corretamente.
        var bot =  janela .bot;

        // Configurações de carga personalizados fixado abaixo
        bot.retrieveSettings ();

        / *
         Estenda o bot aqui, quer chamando outra função ou aqui diretamente.
         Código Modelo para um comando bot:
         bot.commands.commandCommand = {
         comando: "cmd",
         classificação: 'user / bouncer / mod / manager',
         digite: 'startsWith / exato,
         funcionalidade: function (chat, cmd) {
         if (! this.type === 'exata' && chat.message.length == cmd.length) vazio retorno (0);
         if (! bot.commands.executable (this.rank, chat)) vazio retorno (0);
         else {
         // Funcionalidade Comandos vai aqui.
         }
         }
         }
         * /

        bot.commands.baconCommand = {
            comando :  ' toucinho ' ,   // O comando a ser chamado. Com o comando padrão literal isso seria: o bacon
            Ranking :  ' usuário ' , // permissão mínima do usuário para usar o comando
            Tipo :  ' exata ' , // Especifique se pode aceitar variáveis ​​ou não (se assim for, estes têm de ser tratados-se através da chat.message
            funcionalidade : função ( bate-papo , cmd ) {
                se ( este . tipo  ===  ' exata '  && chat.message. comprimento  ==! cmd. comprimento ) retorno  nulo ( 0 );
                se ( ! bot.commands.executable ( este .rank, chat)) retorno  nulo ( 0 );
                outra coisa {
                    API.sendChat ( " / me Bacon !!! " );
                }
            }
        };

        // Carrega o pacote de bate-papo novamente ter em conta quaisquer alterações
        bot.loadChat ();

    }

    // Altere as configurações bots padrão e verifique se eles são carregados na inicialização

    localStorage.setItem ( " basicBotsettings " , JSON.stringify ({
        botname :  " BOTBABACA " ,
        língua :  " Inglês " ,
        chatLink :  " http://rawgit.com/italocjs/basicBot/master/lang/en.json " ,
        maximumAfk :  120 ,
        afkRemoval :  verdadeiro ,
        maximumDc :  30 ,
        bouncerPlus :  false ,
        lockdownEnabled :  false ,
        LockGuard :  false ,
        maximumLocktime :  10 ,
        cycleGuard :  verdadeiro ,
        maximumCycletime :  10 ,
        TIMEGUARD : Verdadeiro ,
        maximumSongLength :  6 ,
        autodisable :  verdadeiro ,
        commandCooldown :  10 ,
        usercommandsEnabled :  verdadeiro ,
        lockskipPosition :  3 ,
        lockskipReasons : [
            [ " tema " , " Essa musica this na Lista dos generos Proibidos, escolhe Outra jumento " ],
            [ " op " , " Essa musica toca Demais caraio, escolhe Outra " ],
            [ " historico " , " Essa musica ta nenhum animal historico, como sou bonzinho vou deixar tu escolher Outra " ],
            [ " misturar " , " Você jogou um mix, que é contra as regras. " ],
            [ " som " , " A canção que você jogou teve má qualidade do som ou nenhum som. " ],
            [ " NSFW " , " TA ACHANDO QUE AQUI E Xvideos PORRA? escolhe Outra " ],
            [ " indisponíveis " , " A canção que você jogou não estava disponível para alguns usuários. " ]
        ],
        afkpositionCheck :  3 ,
        afkRankCheck :  " embaixador " ,
        motdEnabled :  verdadeiro ,
        motdInterval :  5 ,
        motd :  " Vai Tomar proibição ^ " ,
        filterChat :  verdadeiro ,
        etaRestriction :  false ,
        boas-vindas :  false ,
        Oplink :  nulo ,
        rulesLink :  nulo ,
        themeLink :  nulo ,
        fbLink :  nulo ,
        youtubeLink :  nulo ,
        website :  nulo ,
        intervalMessages : [],
        messageInterval :  5 ,
        songstats :  falsos ,
        commandLiteral :  " ! " ,
        blacklists : {
            NSFW :  " https://rawgit.com/italocjs/pdubot/master/blacklists/nsfw.json " ,
            OP :  " https://rawgit.com/Yemasthui/basicBot-customization/master/blacklists/ExampleOPlist.json "
        }
    }));

    // Iniciar o bot e estendê-lo quando ele foi carregado.
    .getScript $ ( ' https://rawgit.com/italocjs/basicBot/master/basicBot.js ' , estender);

.}) chamada ( este );
