# OS4V — downloads

**OS4V** (*OpenScience for Vision*) é a interface dos equipamentos de
imageamento hiperespectral da OpenScience.

Este repositório existe só para **distribuir o instalador**. O código-fonte não
está aqui.

## Baixar

Pegue o instalador mais recente em **[Releases](../../releases/latest)**.

O arquivo se chama `OS4V_Setup_<versão>.exe`. Baixe, execute e siga o
assistente. Não é necessário desinstalar a versão anterior: o instalador
atualiza no lugar, e seus dados — cubos espectrais, calibrações, arquivos
`.nucset` e gabaritos de macro — não são tocados.

## O aviso do Windows na primeira execução

O instalador **não é assinado digitalmente**, então o Windows vai mostrar uma
tela dizendo *"O Windows protegeu o seu PC"*. Isso não indica que o arquivo
tenha problema — indica que ele ainda não acumulou reputação no SmartScreen.

Para prosseguir: clique em **Mais informações** e depois em **Executar assim
mesmo**.

Durante a instalação o Windows vai pedir permissão de administrador duas vezes,
para dois componentes necessários:

1. o **runtime do Visual C++** — sem ele o OS4V não abre;
2. o **driver da câmera Baumer** — sem ele a câmera não é reconhecida.

Se o seu antivírus colocar o arquivo em quarentena, libere-o pelo próprio
antivírus antes de executar.

## Atualizações

A partir da versão 0.2, o OS4V **avisa sozinho** quando sai uma versão nova:
aparece um aviso discreto na janela, ao lado do número da versão instalada, com
a opção de atualizar ali mesmo. O download é verificado por SHA-256 antes de ser
executado.

A checagem acontece uma vez a cada abertura do programa e é **silenciosa**: se o
equipamento estiver sem rede, nada é exibido e nada é interrompido. Também há um
link **"Procurar atualizações"** para consultar na hora.

O botão **"Depois"** dispensa o aviso daquela versão específica. Você volta a ser
avisado quando sair outra.

## Voltar para uma versão anterior

As versões antigas continuam disponíveis em
[Releases](../../releases) — nenhuma é removida.

Para voltar, baixe o instalador da versão desejada e execute. Ele sobrescreve a
instalação atual, e seus dados seguem intactos.

## Ao relatar um problema

Anexe o arquivo de log, que é o único artefato com informação real sobre o que
aconteceu:

```
C:\OS4V\application.log
```

Informe também a **versão instalada**, que aparece na própria janela do OS4V, no
canto com o nome do programa.

## Licença

O OS4V é software proprietário da OpenScience. Os termos acompanham a
instalação, em `C:\OS4V\LICENSE.txt`.

Ele inclui componentes de terceiros — entre eles Qt (LGPL-3), libusb (LGPL-2.1)
e o runtime do Baumer GAPI SDK — cujos avisos, atribuições e informações de
obtenção de código-fonte estão em `C:\OS4V\THIRD-PARTY-NOTICES.txt`, também
instalado junto ao programa.
