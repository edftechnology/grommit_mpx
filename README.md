# Como configurar/instalar/usar o `gromit-mpx` no `Linux Ubuntu`

## Resumo

Neste documento estão contidos os principais comandos e configurações para instalar e usar o `gromit-mpx` via `apt` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings to install and use `gromit-mpx` via `apt` on `Linux Ubuntu`._


## Descrição [2][3]

### `gromit-mpx`

O `Gromit-MPX` é uma ferramenta de anotação em tela para ambientes gráficos Unix, incluindo sessões `X11` e sessões `Wayland` com `XWayland`. Ele permite desenhar sobre aplicativos em execução, destacar áreas da tela durante apresentações, limpar as anotações, alternar a visibilidade dos desenhos e ajustar atalhos e ferramentas de desenho por arquivo de configuração.


## 1. Como instalar o `gromit-mpx` no `Linux Ubuntu` via `apt` [1][2]

Para instalar o `gromit-mpx` no `Linux Ubuntu` usando o gerenciador de pacotes `apt`, você pode seguir estes passos:

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

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt update
    ```

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes:
    ```bash
    sudo apt --fix-broken install
    ```

    2.6 Limpar o `cache` do gerenciador de pacotes `apt` novamente:
    ```bash
    sudo apt clean
    ```

    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt list --upgradable
    ```

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`:
    ```bash
    sudo apt full-upgrade -y
    ```

## 1.2 Instalar e usar o `gromit-mpx`

Após atualizar o sistema, instale o pacote oficial disponível nos repositórios do `Ubuntu`:

1. Instalar o `gromit-mpx` via `apt`:

    ```bash
    sudo apt install gromit-mpx -y
    ```

2. Verificar se o comando foi instalado corretamente:

    ```bash
    gromit-mpx --version
    ```

3. Iniciar o `gromit-mpx`:

    ```bash
    gromit-mpx
    ```

    O `gromit-mpx` fica em execução em segundo plano e pode ser ativado por atalhos de teclado ou por novas chamadas ao comando. Para encerrar o processo principal pelo terminal, execute:

    ```bash
    gromit-mpx --quit
    ```

    O arquivo de configuração do usuário normalmente fica em `~/.config/gromit-mpx.cfg`. Se esse arquivo não existir, o programa usa a configuração padrão instalada em `/etc/gromit-mpx/`.


### 1.2.1 Teclas de atalho do `gromit-mpx`

<div align="center">

| _Description_     | Descrição             | Tecla de atalho padrão |
|:------------------|:----------------------|:----------------------:|
| Toggle painting   | Alternar pintura      | `F9`                   |
| Clear screen      | Limpar tela           | `Shift + F9`           |
| Toggle visibility | Alternar visibilidade | `Ctrl + F9`            |
| Undo              | Desfazer              | `F8`                   |
| Redo              | Refazer               | `Shift + F8`           | 
| Quit              | Sair                  | `Alt + F9`             |

</div>

## 2. Código completo para configurar/instalar/usar

Para instalar o `gromit-mpx` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abrir o `Terminal Emulator`. Você pode fazer isso pressionando:

    ```bash
    Ctrl + Alt + T
    ```

2. Digite o seguinte comando e pressione `Enter`:

    ```bash
    sudo apt clean
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install -y
    sudo apt autoclean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo apt install gromit-mpx -y
    gromit-mpx --version
    ```


## Referências

[1] OPENAI. **Instalar o `gromit-mpx` no `linux ubuntu` pelo `terminal emulator`**. Disponível em: <https://chatgpt.com/g/g-p-6980caf949648191ad6acfcdbe590f9e-instalar/c/7c35ad4d-d9c9-4498-9837-ab1b99548eb5>. ChatGPT. Acessado em: 07/09/2026.

[2] CANONICAL. **Gromit-mpx - presentation helper to make annotations on screen**. Disponível em: <https://manpages.ubuntu.com/manpages/jammy/man1/gromit-mpx.1.html>. Acessado em: 07/09/2026.

[3] BEIER, Christian. **Gromit-mpx**. Disponível em: <https://github.com/bk138/gromit-mpx>. GitHub. Acessado em: 07/09/2026.

