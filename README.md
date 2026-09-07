# Como configurar/instalar/usar o `gromit-mpx` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `gromit-mpx` no `Linux Ubuntu`.

## _Abstract_

_In this document are contained the main commands and settings to set up/install the `gromit-mpx` on `Linux Ubuntu`._


## Descrição [2]

### `gromit-mpx`

O `Gromit-MPX` é uma ferramenta de desenho em tela aberta projetada para permitir que os usuários desenhem e escrevam diretamente na área de trabalho do computador. Ele oferece uma variedade de opções de pincel e cores, além de suporte para entrada de caneta ou tela sensível ao toque. Com recursos como ocultar temporariamente as anotações e ajustar a opacidade, é ideal para apresentações, tutoriais e colaboração em equipe durante reuniões virtuais.


## 1. Como configurar/instalar/usar o `gromit-mpx` no `Linux Ubuntu` [1]

Para configurar/instalar/usar o `gromit-mpx` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando:
    ```bash
    sudo apt clean
    ```
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do `cache` local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando:
    ```bash
    sudo apt autoclean
    ```

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando:
    ```bash
    sudo apt autoremove -y
    ```

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update -y`

    2.5 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.6 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update -y`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`

    2.7 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.8 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

## 1.2 Usar o `gromit-mpx`

Para instalar o gromit-mpx no Linux Ubuntu, você pode seguir os seguintes passos:

1. **Instale o gromit-mpx executando:** `sudo apt install gromit-mpx -y`

    Após a instalação, você pode iniciar o `gromit-mpx` diretamente do terminal ou configurá-lo para iniciar automaticamente com o sistema. O `gromit-mpx` permite que você desenhe em sua tela, o que pode ser particularmente útil para apresentações ou para destacar algo enquanto você grava sua tela.

    Caso deseje iniciar o `gromit-mpx`, você pode simplesmente digitar `gromit-mpx` no `Terminal Emulator`. Para ativar e desativar o desenho, você geralmente usa a tecla de atalho padrão que é o `F9`. Você pode configurar as teclas de atalho e outras opções editando o arquivo de configuração do `gromit-mpx`, geralmente localizado em `~/.config/gromit-mpx.cfg`.

Lembre-se de que, para fazer anotações durante uma apresentação ou enquanto usa outros aplicativos, o `gromit-mpx` deve estar rodando em segundo plano. Você também pode querer consultar a documentação ou a página de ajuda do `gromit-mpx` para obter mais informações sobre personalizações e uso 

### 1.2.1 Teclas de atalho do `grommit-mpx`

<div align="center">

| _Description_     | Descrição             | Tecla de atalho |
|:------------------|:----------------------|:---------------:|
| Toggle painting   | Alternar pintura      | `Home`          |
| Clear screen      | Limpar tela           | `Shift + Home`  |
| Toggle visibility | Alternar visibilidade | `Ctrl + Home`   |
| Undo              | Desfazer              | `End`           |
| Redo              | Refazer               | `Shift + End`   | 
| Quit              | Sair                  | `Alt + Home`    |

</div>

## 2. Código completo para configurar/instalar/usar

Para configurar/instalar/usar o `gromit-mpx` no `Linux Ubuntu`sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```bash
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove
    sudo apt update -y
    sudo apt autoclean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install gromit-mpx -y
    gromit-mpx
    ```


## Referências

[3] OPENAI.
**Instale gromit-mpx no Ubuntu.**
Disponível em: <https://chat.openai.com/c/7c35ad4d-d9c9-4498-9837-ab1b99548eb5> (texto adaptado).
Acessado em: 06/03/2024 13:47.

[2] OPENAI.
**Vs code: editor popular.**
Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado).
Acessado em: 06/03/2024 13:48.

