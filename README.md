<!DOCTYPE html>
<html lang="pt">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instalar Evil-WinRM no Debian</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }
        h1 {
            color: #333;
        }
        h2 {
            color: #555;
        }
        pre {
            background-color: #f4f4f4;
            border-left: 3px solid #333;
            padding: 10px;
            overflow-x: auto;
        }
        code {
            font-family: monospace;
            background-color: #f4f4f4;
            padding: 2px 4px;
            border-radius: 4px;
        }
    </style>
</head>
<body>
    <h1>Instalar Evil-WinRM no Debian</h1>
    <h2>1. Instalar Dependências</h2>
    <p>Primeiro, certifique-se de que seu sistema está atualizado e tem as dependências necessárias instaladas.</p>
    <pre><code>sudo apt update
sudo apt upgrade
sudo apt install -y ruby ruby-dev build-essential</code></pre>
    <h2>2. Instalar o Evil-WinRM</h2>
    <p>O Evil-WinRM pode ser instalado diretamente usando o RubyGems, que é o gerenciador de pacotes para Ruby.</p>
    <pre><code>sudo gem install evil-winrm</code></pre>
    <h2>3. Verificar a Instalação</h2>
    <p>Após a instalação, você pode verificar se o Evil-WinRM foi instalado corretamente e verificar a versão instalada:</p>
    <pre><code>evil-winrm --version</code></pre>
    <h2>4. Uso Básico do Evil-WinRM</h2>
    <p>Para usar o Evil-WinRM, você precisará do endereço IP do computador Windows, do nome de usuário e da senha. O comando básico para iniciar uma sessão é:</p>
    <pre><code>evil-winrm -i &lt;IP_DO_COMPUTADOR_WINDOWS&gt; -u &lt;USUARIO&gt; -p &lt;SENHA&gt;</code></pre>
    <p>Aqui está um exemplo:</p>
    <pre><code>evil-winrm -i 192.168.1.10 -u Administrator -p 'Senha123'</code></pre>
    <h2>5. Configuração Adicional</h2>
    <p>Dependendo do ambiente de segurança e das configurações de WinRM no sistema Windows alvo, você pode precisar ajustar algumas configurações, como desativar a autenticação NTLM ou permitir o tráfego WinRM.</p>
    <p>Para ambientes de teste, pode ser necessário configurar o Windows para aceitar conexões WinRM. Normalmente, você pode fazer isso no Windows com o seguinte comando PowerShell executado como administrador:</p>
    <pre><code>winrm quickconfig</code></pre>
    <h2>6. Resolução de Problemas</h2>
    <p>Se você encontrar problemas, verifique as mensagens de erro e consulte a documentação ou fóruns de suporte. Problemas comuns podem envolver configurações de firewall, permissões, ou configurações de WinRM no alvo.</p>
    <h2>7. Comando Adicional</h2>
    <p>Para se conectar ao alvo usando um hash de administrador local, você pode usar o seguinte comando:</p>
    <pre><code>evil-winrm -u Administrator -H &lt;Local Admin Hash&gt; -i MACHINE_IP</code></pre>
    <p>Substitua <code>&lt;Local Admin Hash&gt;</code> pelo hash do administrador local e <code>MACHINE_IP</code> pelo IP da máquina alvo.</p>
    <p>Isso deve cobrir a instalação e o uso básico do Evil-WinRM em um sistema Debian. Se precisar de funcionalidades avançadas, consulte a <a href="https://github.com/Hackplayers/evil-winrm" target="_blank">documentação oficial do Evil-WinRM</a> para ajustes adicionais.</p>
</body>
</html>
