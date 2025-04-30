<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Teste Talkdesk Chat</title>
</head>
<body>
  <h1>Chat Talkdesk</h1>
  <p>Se o chat foi carregado corretamente, o botão/flutuante aparecerá no canto da tela.</p>

  <!-- Start of Talkdesk Code -->
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
      };
    })(
      window,
      document,
      "tdWebchat",
      {
        touchpointId: "c589db0d311c4ea18748755796e2dafe", // substitua pelo seu touchpoint real se necessário
        accountId: "",
        region: "td-us-1"
      },
      {
        enableValidation: false,
        enableEmoji: true,
        enableUserInput: true,
        enableAttachments: true
      }
    );
  </script>
  <!-- End of Talkdesk Code -->
</body>
</html>
