# 🛸 Metaverse-Nav-Log (Linux & SO)

Bem-vindo ao log de navegação do Metaverso! Este diretório é o núcleo das minhas anotações, mapas mentais e documentações práticas sobre **Linux, Administração de Sistemas e Shell/Bash**.

Aqui é onde organizo guias visuais e materiais de consulta rápida para o uso do sistema no dia a dia.

---

## 🐧 1. Comandos Linux Bash Shell

> **Módulo:** Metaverse-Nav-Log (Linux & SO)  
> **Ambiente de Testes:** Fedora Linux (VM)  
> **Status:** Desespero (porém progredindo) 🚀

### 📌 Sobre este Guia
Este guia reúne desde a navegação básica no terminal até comandos avançados de diagnóstico de sistema, rede, manipulação de links, metacaracteres e compactação de arquivos.

### 🛠️ Conteúdos & Comandos Mapeados

* 💻 **Informações do Sistema & Diagnóstico:** `whoami`, `date`, `uname -a`, `hostname`, `top`, `ps aux`, `free -h`, `df -h`
* 🌐 **Comandos de Rede:** `ip a`, `ifconfig`, `ping`, `traceroute`, `nslookup`, `netstat -tulnp`, `curl`
* 📁 **Navegação & Estrutura de Diretórios:** `cd`, `cd -P` *(navegação física vs. lógica)*, `pwd`, `mkdir` (`-p`), `touch`, `rm` (`-rf`)
* 📄 **Manipulação de Arquivos & Links:** `mv` (`-v`), `cp` (`-r`), `ln` *(Hard Link)* e `ln -s` *(Soft Link em arquivos e diretórios)*
* 📋 **Listagem & Exibição:** `ls`, `ls -l`, `ls -a`, `ls -la`, `ls -i1` *(Inodes)*, `ls -R` *(listagem recursiva)*
* 🧩 **Metacaracteres, Operadores & Expansão:** Wildcards (`*`, `?`, `[ ]`), expansão de chaves (`{ }`), encadeamento de comandos (`;`)
* 📊 **Leitura, Análise & Redirecionamento:** `wc` (`-l`, `-w`, `-c`, `-m`, `-L`), redirecionadores (`>`, `>>`, `<`)
* 🔍 **Localização & Filtros:** `grep` (`-i`), `find` (`-ls`, `-size`), `locate` / `plocate`
* 📦 **Empacotamento & Compactação:** `tar` (`-cvf`, `-czvf`, `-xvf`, `-zxvf`, `-tvf`, `--wildcards`), `gzip` e `gunzip` (`-d`, `-c`, `-k`)

📄 **[Download / Visualizar o Mapa Mental de Códigos Linux (PDF)](./Comandos%20Terminal%20Linux/Mapa%20Mental%20Codigos%20Linux.pdf)**

---

## 🐚 2. Shell Linux & Gerenciamento de Processos

> **Módulo:** Metaverse-Nav-Log (Linux & SO)  
> **Ambiente de Testes:** Fedora Linux (VM)  
> **Status:** Ta ai

### 📌 Sobre este Guia
Mapeamento dos conceitos fundamentais do interpretador de comandos Bash, o funcionamento de variáveis (locais vs. ambiente), arquivos de configuração do sistema e o controle de processos/jobs no terminal.

### 🛠️ Conteúdos & Conceitos Mapeados

#### 1. Informações Gerais
* 🐚 **O que é Shell/Bash:** A interface que atua como ponte de comunicação entre as aplicações e o Kernel do Linux.
* 📦 **Variáveis Locais x Ambiente (Global):**
  * **Local** (`VAR="valor"`): Isolada na aba atual. Scripts e sub-processos não têm acesso.
  * **Global** (`export VAR="valor"`): Exportada para a tabela de ambiente. Herda e fica visível para scripts e processos filhos iniciados naquela sessão.
* ⚙️ **Modificando a BASH:**
  * Para todos os usuários: `/etc/profile`
  * Apenas para o seu usuário: `~/.bashrc` ou `~/.profile` (editáveis via `nano`, visíveis com `ls -a`).
  * Listar variáveis de ambiente: Comando `env`.

#### 2. Recursos Avançados & Controle da Shell
* 🔍 `$PATH`: Guarda a ordem de pesquisa dos diretórios onde o sistema busca os executáveis dos comandos.
* 📝 `$EDITOR`: Define o editor de texto padrão (ex: `nano`, `vim`) acionado automaticamente por outras ferramentas (`git`, `crontab`).
* 📊 **`SET` X `ENV`:**
  * `set`: Exibe **todas** as variáveis e funções da Shell (locais + globais).
  * `env`: Exibe **apenas** as variáveis de ambiente (globais).
* ⚡ **`ALIAS`:** Criação de atalhos para comandos extensos ou rotineiros (ex: `alias c='clear'`). Execute `alias` sozinho para ver todos os atalhos ativos.
* 🎛️ **`JOBS` e o Trio de Controle (`Ctrl+Z`, `bg`, `fg`):**
  * `jobs`: Gerenciador de tarefas da aba atual (mostra o ID do job, estado pausado ou em background).
  * `Ctrl + Z`: Congela/pausa o processo atual em *foreground*.
  * `bg %ID`: Reativa o job para rodar em segundo plano (*background*).
  * `fg %ID`: Traz o job de volta para o primeiro plano (*foreground*).
  * `kill %ID`: Encerra o job informado (obrigatório o uso do `%` para indicar que é um Job e não o PID do sistema).

📄 **[Visualizar Mapa Mental - Shell Linux (PDF)](./SHELL/Shell%20Linux.pdf)**

---

## 🎯 Radar de Estudos

- [x] Comandos essenciais de terminal, redes e compactação (`tar` / `gzip`)
- [x] Variáveis de ambiente, arquivos de configuração do Bash e controle de Jobs
- [ ] Permissões de arquivos (`chmod`, `chown`, modo octal)
- [ ] Shell Scripting (Lógica de automação com Bash)

---

*"Tenho certeza que ninguém lê isso, então vou dizer nada. 🐊"*
