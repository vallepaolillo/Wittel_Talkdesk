
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wittel - Soluções em Comunicação</title>
    <style>
        body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
        header { background: #002856; color: white; padding: 20px; text-align: center; }
        nav ul { list-style-type: none; padding: 0; margin: 0; display: flex; justify-content: center; background: #004080; }
        nav ul li { margin: 0 15px; }
        nav ul li a { color: white; text-decoration: none; font-weight: bold; }
        section.hero { background: url('https://wittel.com/wp-content/uploads/2021/06/solucoes-contact-center.jpg') no-repeat center center/cover; color: white; padding: 100px 20px; text-align: center; }
        section.content { padding: 40px 20px; }
        footer { background: #002856; color: white; padding: 20px; text-align: center; }
    </style>
</head>
<body>
    <header>
        <h1>Wittel</h1>
        <p>Soluções em Comunicação para sua Empresa</p>
    </header>
    <nav>
        <ul>
            <li><a href="#">Início</a></li>
            <li><a href="#">Soluções</a></li>
            <li><a href="#">Clientes</a></li>
            <li><a href="#">Contato</a></li>
        </ul>
    </nav>
    <section class="hero">
        <h2>Transforme sua comunicação corporativa</h2>
        <p>Inovação, tecnologia e excelência no atendimento ao cliente.</p>
    </section>
    <section class="content">
        <h3>Sobre a Wittel</h3>
        <p>A Wittel oferece soluções completas de comunicação, com foco em performance, segurança e experiência do cliente.</p>
        
        <h3>Contato</h3>
        <p>Email: contato@wittel.com</p>
        <p>Telefone: +55 11 3879-3000</p>
        <p>Endereço: Av. Francisco Matarazzo, 1500 – Água Branca, São Paulo – SP</p>
    </section>
    <footer>
        <p>© 2025 Wittel Comunicação. Todos os direitos reservados.</p>
    </footer>

    <!-- Código do Bot da Talkdesk -->
  <script>
      var webchat;
      (function(window, document, node, props, configs) {
        if (window.TalkdeskChatSDK) {
          console.error("TalkdeskChatSDK already included");
          return;
        }
        var divContainer = document.createElement("div");
        divContainer.id = node;
        document.body.appendChild(divContainer);
        var src = "https://talkdeskchatsdk.talkdeskapp.com/v2/talkdeskchatsdk.js";
        var script = document.createElement("script");
        var firstScriptTag = document.getElementsByTagName("script")[0];
        script.type = "text/javascript";
        script.charset = "UTF-8";
        script.id = "tdwebchatscript";
        script.src = src;
        script.async = true;
        firstScriptTag.parentNode.insertBefore(script, firstScriptTag);
        script.onload = function() {
          webchat = TalkdeskChatSDK(node, props);
          webchat.init(configs);
          /*
           * Send custom data from your website to TalkDesk!
           * If you would like to do it, you need to remove the following commented code and
           * modify the webchat.setContextParam parameters to pass in the data you need.
           */
           /*function setContext() {
             webchat.setContextParam({ "var1": "value1", "var2": "value2", "var3": 100 })
           }
           // Send data when the chat conversation is initiated
           webchat.onConversationStart = function() {
             setContext()
           }
           // Send data when the chat widget is open
           webchat.onOpenWebchat = function() {
             setContext()
           }*/
        };
      })(
        window,
        document,
        "tdWebchat",
        { touchpointId: "18002a8d70f04c7e8ec73f878886daef", accountId: "", region: "td-us-1" },
        { enableValidation: false, enableEmoji: true, enableUserInput: true, enableAttachments: true }
      );
    </script>

</body>
</html>
