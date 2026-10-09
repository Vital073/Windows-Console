O que faz
---------
- Define o Heroic como interface inicial SOMENTE para o usuário atual.
- Grava Shell em HKCU\Software\Microsoft\Windows NT\CurrentVersion\Winlogon.
- Não altera HKEY_LOCAL_MACHINE (HKLM), nem muda o shell das outras contas.
- Não tenta gravar em Policies\System, que pode negar acesso por permissões.
- Não inicia o Explorer automaticamente após entrar nessa conta.
- Alt + F1 abre um menu com: Abrir Heroic, desligar, reiniciar, cancelar uma ação
  de energia agendada e fechar o menu. O Explorer não é uma opção normal do menu.
- Desligar/reiniciar pede confirmação e usa atraso de 10 segundos.
- Ao final da instalação, verifica os valores Shell no Registro e mostra letras
  grandes em verde com “SUCESSO!” ou em vermelho com “NÃO FUNCIONOU”. O CMD aguarda
  Enter ou qualquer tecla antes de fechar.

Instalação
----------
1. Extraia todos os arquivos desta pasta/ZIP.
2. Execute Instalar.bat na conta que usará o Heroic como shell.
3. Se o instalador não localizar o Heroic, selecione o arquivo Heroic.exe.
4. Saia da conta e entre novamente, ou reinicie o Windows, para testar.

Importante
----------
- Este pacote não inclui recurso de restauração automática do Registro.
- “SUCESSO!” confirma que os arquivos foram instalados e o valor Shell do usuário
  atual foi gravado e verificado; o comportamento após entrar novamente deve ser testado.
- Se o Heroic não abrir, Ctrl + Alt + Del permite acessar a tela de segurança do
  Windows. O atalho Alt + F1 depende de o shell auxiliar ter iniciado corretamente.
- Se outro programa já reservou Alt+F1, o script inicia o Explorer como alternativa
  para evitar uma sessão sem interface.
- A configuração depende da instalação desktop do Heroic com um executável Heroic.exe.
- No Registro, Shell é um valor REG_SZ (texto), não REG_BINARY.
