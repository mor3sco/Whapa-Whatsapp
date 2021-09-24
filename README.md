# Whapa-Whatsapp
📖 WhatsApp Parser Toolset 

<p align="center">
  <img  src="https://github.com/B16f00t/whapa/blob/master/doc/whapa.png">
</p>

Atualizado: setembro de 2020

WhatsApp Messenger versão 2.20

O Whapa é um conjunto de ferramentas gráficas forenses para analisar o WhatsApp no ​​Android. Todas as ferramentas foram escritas em Python 3.X e testadas em sistemas Linux e Windows 10.

Nota: O Whapa oferece 10x mais desempenho e menos bugs em sistemas Linux do que em Windows.

O Whapa é incluído como padrão em distribuições como Tsurugi Linux (Digital Forensics) e BlackArch Linux (teste de penetração).

O conjunto de ferramentas Whapa é dividido em quatro ferramentas:

* ** Whapa ** (Analisador de Whatsapp)
* ** Whamerge ** (fusão Whatsapp)
* ** Whagodri ** (Whataspp Google Drive Extractor)
* ** Whacipher ** (criptografia / descriptografia Whatsapp)

Instalação
Você pode baixar a versão mais recente do whapa clonando o repositório GitHub:

git clone https://github.com/B16f00t/whapa.git
então:

pip3 install -r ./doc/requirements.txt

Começar
====
se você usa o sistema Linux:
* python3 whapa-gui.py

se você usa o sistema Windows:
* python whapa-gui.py
ou
* clique em whapa-gui.bat

<p align = "center">
  <img src = "https://raw.githubusercontent.com/B16f00t/whapa/master/doc/software.jpg" width = "720" height = "576">
</p>

WHAPA
====
O whapa.py é um analisador de banco de dados Whatsapp do Android que automatiza o processo e apresenta os dados manipulados pelo banco de dados Sqlite de uma forma que seja compreensível para o analista.
Se você copiar o banco de dados "wa.db" no mesmo diretório do script, o número de telefone será exibido junto com o nome.

Observe que este projeto está em um estágio inicial. Assim, você pode encontrar erros. Use-o por sua própria conta e risco!

WHAMERGE
====
whamerge é uma ferramenta para juntar backups em uma nova base de dados, para poder ser analisada e obter mais informações, como grupos deletados, mensagens, etc ...

Aviso: Não associe bancos de dados restaurados com cópias antigas, pois eles repetem os mesmos ids e a cópia não será feita corretamente.


WHAGODRI
=====
whagodri.py é uma ferramenta que permite aos usuários do WhatsApp no ​​Android extrair seus dados de backup do WhatsApp do Google Drive.

Certifique-se de:
* Baixe a última versão do whapa
* Instale os requisitos
* Definições:

Edite apenas os valores do arquivo./cfg/settings.cfg

[auth]
gmail = alias@gmail.com
passw = sua senha
devid = ID do dispositivo (opcional, se especificado obter mais informações)
celnumbr = BackupPhoneNumber -> Código do país + número do telefone (ex. 3466666666666)
* Se você solicitar, faça login em seu navegador e clique aqui, https://accounts.google.com/DisplayUnlockCaptcha.


Se você deseja usar 2FA (Two Factor Authentication), você terá que ir para o URL: https://myaccount.google.com/apppasswords Em seguida, selecione Aplicativo: Outro. Anote: Whapa, e uma senha será exibida, então você deve escrever a senha no seu settings.cfg.

WHACIPHER
=====
whacipher.py é uma ferramenta que permite descriptografar ou criptografar o banco de dados WhatsApp. Você deve ter a chave do seu telefone para descriptografar e, adicionalmente, um banco de dados criptografado como referência para criptografar um novo banco de dados.

