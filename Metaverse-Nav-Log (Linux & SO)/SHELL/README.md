# 🐚 Shell Linux & Gerenciamento de Processos

> **Módulo:** Metaverse-Nav-Log (Linux & SO)  
> **Ambiente de Testes:** Fedora Linux (VM)  
> **Status:** Ta ai  

---

## 📌 Sobre este Guia

Este diretório contém o **Mapa Mental de Shell Linux** em formato PDF, reunindo os conceitos fundamentais do interpretador de comandos Bash, o funcionamento de variáveis (locais vs. ambiente), arquivos de configuração do sistema e o controle de processos/jobs no terminal.

---

## 🛠️ Conteúdos & Conceitos Mapeados

### 1. Informações Gerais
* 🐚 **O que é Shell/Bash:** A interface que atua como ponte de comunicação entre as aplicações e o Kernel do Linux.
* 📦 **Variáveis Locais x Ambiente (Global):**
  * **Local (`VAR="valor"`):** Isolada na aba atual. Scripts e sub-processos **não** têm acesso.
  * **Global (`export VAR="valor"`):** Exportada para a tabela de ambiente. Herda e fica visível para scripts e processos filhos iniciados naquela sessão.
* ⚙️ **Modificando a BASH:**
  * **Para todos os usuários:** `/etc/profile`
  * **Apenas para o seu usuário:** `~/.bashrc` ou `~/.profile` (editáveis via `Home`, visíveis com `ls -a`).
  * **Listar variáveis de ambiente:** Comando `env`.

### 2. Recursos Avançados & Controle da Shell
* 🔍 **`$PATH`:** Guarda a ordem de pesquisa dos diretórios onde o sistema busca os executáveis dos comandos.
* 📝 **`$EDITOR`:** Define o editor de texto padrão (ex: `nano`, `vim`) acionado automaticamente por outras ferramentas (`git`, `crontab`).
* 📊 **`SET` x `ENV`:**
  * `set`: Exibe **todas** as variáveis e funções da Shell (locais + globais).
  * `env`: Exibe **apenas** as variáveis de ambiente (globais).
* ⚡ **`ALIAS`:** Criação de atalhos para comandos extensos ou rotineiros (ex: `alias c='clear'`). Execute `alias` sozinho para ver todos os atalhos ativos.
* 🎛️ **JOBS e o Trio de Controle (`Ctrl+Z`, `bg`, `fg`):**
  * **`jobs`:** Gerenciador de tarefas da aba atual (mostra o ID do job, estado pausado ou em background).
  * **`Ctrl + Z`:** Congela/pausa o processo atual em foreground.
  * **`bg %ID`:** Reativa o job para rodar em segundo plano (*background*).
  * **`fg %ID`:** Traz o job de volta para o primeiro plano (*foreground*).
  * **`kill %ID`:** Encerra o job informado (obrigatório o uso do `%` para indicar que é um Job e não o PID do sistema).

---

## 🗺️ Visualização do Mapa Mental

Clique no link abaixo para visualizar ou baixar a documentação visual completa:

📄 **[Visualizar Mapa Mental - Shell Linux (PDF)](<./Shell Linux.pdf>)**

---

*É nois 🫩*
