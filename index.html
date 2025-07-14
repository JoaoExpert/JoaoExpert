<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WebChat - Atendimento</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f2f5;
            padding: 20px;
        }

        /* Botão flutuante para abrir o chat */
        .chat-toggle {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.3s ease;
            z-index: 1001;
        }

        .chat-toggle:hover {
            transform: scale(1.1);
        }

        .chat-toggle svg {
            width: 30px;
            height: 30px;
            fill: white;
        }

        /* Container do chat */
        .chat-container {
            position: fixed;
            bottom: 90px;
            right: 20px;
            width: 350px;
            height: 500px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
            display: none;
            flex-direction: column;
            overflow: hidden;
            z-index: 1000;
            animation: slideUp 0.3s ease;
        }

        @keyframes slideUp {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .chat-container.active {
            display: flex;
        }

        /* Header do chat */
        .chat-header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 15px 20px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .chat-header-info {
            display: flex;
            align-items: center;
        }

        .agent-avatar {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            margin-right: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        .agent-details h4 {
            margin: 0;
            font-size: 14px;
        }

        .agent-details p {
            margin: 0;
            font-size: 12px;
            opacity: 0.8;
        }

        .close-chat {
            background: none;
            border: none;
            color: white;
            cursor: pointer;
            font-size: 18px;
            padding: 5px;
        }

        /* Área de mensagens */
        .chat-messages {
            flex: 1;
            padding: 20px;
            overflow-y: auto;
            background: #f8f9fa;
        }

        .message {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-end;
        }

        .message.user {
            justify-content: flex-end;
        }

        .message-bubble {
            max-width: 75%;
            padding: 12px 16px;
            border-radius: 18px;
            font-size: 14px;
            line-height: 1.4;
        }

        .message.bot .message-bubble {
            background: white;
            color: #333;
            border-bottom-left-radius: 6px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .message.user .message-bubble {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-bottom-right-radius: 6px;
        }

        .message-time {
            font-size: 11px;
            opacity: 0.6;
            margin: 5px 10px 0;
        }

        /* Área de digitação */
        .chat-input-area {
            padding: 15px 20px;
            background: white;
            border-top: 1px solid #e1e8ed;
            display: flex;
            align-items: center;
        }

        .chat-input {
            flex: 1;
            border: 1px solid #e1e8ed;
            border-radius: 20px;
            padding: 10px 15px;
            font-size: 14px;
            outline: none;
            resize: none;
            max-height: 80px;
        }

        .chat-input:focus {
            border-color: #667eea;
        }

        .send-button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border: none;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            margin-left: 10px;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.2s ease;
        }

        .send-button:hover {
            transform: scale(1.05);
        }

        .send-button svg {
            width: 20px;
            height: 20px;
            fill: white;
        }

        /* Indicador de digitação */
        .typing-indicator {
            display: none;
            padding: 10px 16px;
            background: white;
            border-radius: 18px;
            margin-bottom: 15px;
            max-width: 75%;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .typing-dots {
            display: flex;
            align-items: center;
        }

        .typing-dots span {
            width: 8px;
            height: 8px;
            background: #667eea;
            border-radius: 50%;
            margin: 0 2px;
            animation: typing 1.4s infinite;
        }

        .typing-dots span:nth-child(2) {
            animation-delay: 0.2s;
        }

        .typing-dots span:nth-child(3) {
            animation-delay: 0.4s;
        }

        @keyframes typing {
            0%, 60%, 100% {
                transform: translateY(0);
            }
            30% {
                transform: translateY(-10px);
            }
        }

        /* Responsivo */
        @media (max-width: 480px) {
            .chat-container {
                width: calc(100% - 40px);
                right: 20px;
                left: 20px;
                height: 80vh;
            }
        }
    </style>
</head>
<body>
    <!-- Botão flutuante para abrir o chat -->
    <button class="chat-toggle" onclick="toggleChat()">
        <svg viewBox="0 0 24 24">
            <path d="M20,2H4A2,2 0 0,0 2,4V22L6,18H20A2,2 0 0,0 22,16V4A2,2 0 0,0 20,2M6,9V7H18V9H6M14,11V13H6V11H14M18,15H6V17H18V15Z"/>
        </svg>
    </button>

    <!-- Container do chat -->
    <div class="chat-container" id="chatContainer">
        <!-- Header -->
        <div class="chat-header">
            <div class="chat-header-info">
                <div class="agent-avatar">S</div>
                <div class="agent-details">
                    <h4>Suporte Suri</h4>
                    <p>Online - Responde em alguns minutos</p>
                </div>
            </div>
            <button class="close-chat" onclick="toggleChat()">✕</button>
        </div>

        <!-- Mensagens -->
        <div class="chat-messages" id="chatMessages">
            <div class="message bot">
                <div class="message-bubble">
                    Olá! 👋 Sou o assistente virtual da Suri. Como posso ajudá-lo hoje?
                </div>
            </div>
            <div class="message-time">Agora</div>

            <!-- Indicador de digitação -->
            <div class="typing-indicator" id="typingIndicator">
                <div class="typing-dots">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </div>
        </div>

        <!-- Área de input -->
        <div class="chat-input-area">
            <textarea 
                class="chat-input" 
                id="chatInput" 
                placeholder="Digite sua mensagem..."
                rows="1"
                onkeypress="handleKeyPress(event)"
            ></textarea>
            <button class="send-button" onclick="sendMessage()">
                <svg viewBox="0 0 24 24">
                    <path d="M2,21L23,12L2,3V10L17,12L2,14V21Z"/>
                </svg>
            </button>
        </div>
    </div>

    <script>
        let chatOpen = false;

        function toggleChat() {
            const chatContainer = document.getElementById('chatContainer');
            chatOpen = !chatOpen;
            
            if (chatOpen) {
                chatContainer.classList.add('active');
                document.getElementById('chatInput').focus();
            } else {
                chatContainer.classList.remove('active');
            }
        }

        function sendMessage() {
            const input = document.getElementById('chatInput');
            const message = input.value.trim();
            
            if (message === '') return;
            
            // Adicionar mensagem do usuário
            addMessage(message, 'user');
            input.value = '';
            
            // Simular resposta do bot
            showTypingIndicator();
            
            setTimeout(() => {
                hideTypingIndicator();
                const responses = [
                    'Obrigado pela sua mensagem! Em que posso ajudá-lo?',
                    'Entendi! Vou transferir você para um de nossos especialistas.',
                    'Essa é uma ótima pergunta! Deixe-me verificar as informações para você.',
                    'Perfeito! Vou processar sua solicitação agora mesmo.',
                    'Posso sim te ajudar com isso! Qual seria a melhor forma de contato?'
                ];
                const randomResponse = responses[Math.floor(Math.random() * responses.length)];
                addMessage(randomResponse, 'bot');
            }, 2000);
        }

        function addMessage(text, sender) {
            const messagesContainer = document.getElementById('chatMessages');
            const messageDiv = document.createElement('div');
            messageDiv.className = `message ${sender}`;
            
            const now = new Date();
            const timeString = now.toLocaleTimeString('pt-BR', { 
                hour: '2-digit', 
                minute: '2-digit' 
            });
            
            messageDiv.innerHTML = `
                <div class="message-bubble">${text}</div>
            `;
            
            const timeDiv = document.createElement('div');
            timeDiv.className = 'message-time';
            timeDiv.textContent = timeString;
            
            messagesContainer.insertBefore(messageDiv, document.getElementById('typingIndicator'));
            messagesContainer.insertBefore(timeDiv, document.getElementById('typingIndicator'));
            
            // Scroll para baixo
            messagesContainer.scrollTop = messagesContainer.scrollHeight;
        }

        function showTypingIndicator() {
            document.getElementById('typingIndicator').style.display = 'block';
            const messagesContainer = document.getElementById('chatMessages');
            messagesContainer.scrollTop = messagesContainer.scrollHeight;
        }

        function hideTypingIndicator() {
            document.getElementById('typingIndicator').style.display = 'none';
        }

        function handleKeyPress(event) {
            if (event.key === 'Enter' && !event.shiftKey) {
                event.preventDefault();
                sendMessage();
            }
        }

        // Auto-resize do textarea
        document.getElementById('chatInput').addEventListener('input', function() {
            this.style.height = 'auto';
            this.style.height = Math.min(this.scrollHeight, 80) + 'px';
        });

        // Fechar chat ao clicar fora
        document.addEventListener('click', function(event) {
            const chatContainer = document.getElementById('chatContainer');
            const chatToggle = document.querySelector('.chat-toggle');
            
            if (chatOpen && 
                !chatContainer.contains(event.target) && 
                !chatToggle.contains(event.target)) {
                toggleChat();
            }
        });
    </script>
</body>
</html>
