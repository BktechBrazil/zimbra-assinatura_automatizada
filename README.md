# assinatura_automatizada

English version: https://github.com/Zimbra-Community/signature-template

(pt_BR)
Através desse Zimlet, que é distribuído como open source, é possível definir uma assinatura padrão para a organização, e os usuários inserem os seus dados diretamente no cliente web. desenvolvido pela Bktech (http://www.bktech.com.br) em parceria com a Zeta Alliance (https://zetalliance.org). Versão em português brasileiro (pt_BR). Compatível a partir da versão 8.7 do Zimbra.

### INSTALAÇÃO

-  su - zimbra
-  cd /tmp
-  git clone https://github.com/BktechBrazil/assinatura_automatizada.git
-  cd assinatura_automatizada
-  Para utilizar o próprio servidor Zimbra para armazenar a imagem da assinatura, copie a imagem que deseja utilizar para o diretório /opt/zimbra/jetty/webapps/zimbra/public
-  A URL será como o exemplo: https://seuservidor.seudominio.com.br/public/exemplo.png
-  Se o ambiente for Multi-Server, execute o mesmo procedimento em todos os servidores Mailbox
-  Edite o arquivo signatureZimlet.js alterando a URL nas linhas 46 e 113
-  Criar o arquivo do zimlet com o comando: zip -x README.md -r com_zimbra_signature_zimlet.zip *
-  Copiar o zimlet (com_zimbra_signature_zimlet.zip) para o diretório /opt/zimbra/zimlets
-  Efetuar o deploy com o comando : zmzimletctl deploy com_zimbra_signature_zimlet.zip
-  Limpar o cache do zimlet com o comando: zmprov fc zimlet
-  Habilitar o zimlet para as classes de serviço ou contas desejadas

### License

Copyright (C) 2017  Barry de Graaff [Zeta Alliance](http://www.zetalliance.org/)

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see http://www.gnu.org/licenses/.
