# 🚀 Iniciante Linux - Guia Prático para Ubuntu

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)  
[![Contribuições Bem-vindas](https://img.shields.io/badge/Contribua-Sim-brightgreen.svg)](CONTRIBUTING.md)  

![Linux Banner](https://img.shields.io/badge/Linux-Ubuntu-0078D6?style=for-the-badge&logo=ubuntu)

---

## 📑 Sumário

1. [Introdução](#1-introdução)
2. [Iniciando com o Ubuntu](#2-iniciando-com-o-ubuntu)
3. [Comandos Básicos do Linux Explicados](#3-comandos-básicos-do-linux-explicados)
4. [Dicas e Truques para Produtividade](#4-dicas-e-truques-para-produtividade)
5. [10 Scripts Indispensáveis para Programadores](#5-10-scripts-indispens%C3%A1veis-para-programadores)
6. [Bash vs. Zsh: Diferenças, Instalação & Recomendações](#6-bash-vs-zsh-diferen%C3%A7as-instala%C3%A7%C3%A3o--recomenda%C3%A7%C3%B5es)
7. [Criando Seu Próprio Script (Bash e Zsh)](#7-criando-seu-pr%C3%B3prio-script-bash-e-zsh)
8. [Recursos Adicionais](#8-recursos-adicionais)
9. [Conclusão](#9-conclus%C3%A3o)

---

## 1. Introdução

👋 **Olá, seja bem-vindo ao Iniciante Linux Master!**  
Este guia foi criado para te ajudar a desmistificar a linha de comando no Ubuntu e te transformar num usuário muito mais produtivo. Aqui, vamos explicar passo a passo como usar os comandos e o porquê de cada um deles, para que você se sinta seguro e confiante.

---

## 2. Iniciando com o Ubuntu

### Passo a Passo de Instalação

1. **Baixe o Ubuntu:**  
   Visite a [página oficial do Ubuntu](https://ubuntu.com/download/desktop) e baixe a versão LTS mais recente.

2. **Crie um USB Bootável:**  
   Use ferramentas como [Rufus](https://rufus.ie/). Se preferir, assista a este [tutorial no YouTube](https://www.youtube.com/watch?v=mXyN1aJYefc&t=1s) para facilitar.

3. **Instale o Ubuntu:**  
   Reinicie seu computador a partir do USB e siga as instruções na tela para instalar o Ubuntu.

---

## 3. Comandos Básicos do Linux Explicados

Confira esta tabela com os comandos mais usados e suas principais opções:

| **Comando** | **Exemplo**                                | **O que ele faz?**                                                                                   |
|-------------|--------------------------------------------|------------------------------------------------------------------------------------------------------|
| `ls`        | `ls -l`                                    | Lista os arquivos em um formato detalhado. A opção `-l` significa "lista longa".                     |
| `cp`        | `cp -r pasta_origem pasta_destino`         | Copia arquivos ou diretórios. A opção `-r` copia recursivamente, ou seja, tudo dentro da pasta.       |
| `rm`        | `rm -f arquivo`                            | Remove um arquivo sem perguntar confirmação. O `-f` significa "forçar".                              |
| `mv`        | `mv arquivo novo_nome`                     | Move ou renomeia arquivos e diretórios.                                                              |
| `grep`      | `grep -i "texto" arquivo`                  | Procura por um texto, ignorando diferenças entre maiúsculas e minúsculas (opção `-i`).                 |
| `man`       | `man ls`                                   | Abre o manual do comando `ls`, mostrando todas as opções disponíveis.                                |
| `chmod`     | `chmod +x script.sh`                       | Torna um script executável. A opção `+x` adiciona permissão de execução.                             |
| `chown`     | `chown user:group arquivo`                 | Muda o dono e o grupo de um arquivo.                                                                 |
| `find`      | `find . -name "*.txt"`                     | Procura arquivos com a extensão `.txt` a partir do diretório atual.                                  |
| `tar`       | `tar -czvf arquivo.tar.gz pasta`           | Cria um arquivo compactado. Aqui, `-c` cria, `-z` usa gzip, `-v` mostra o progresso e `-f` define o nome. |

### Tabela de Flags Comuns e Importantes

Aqui estão algumas opções (flags) úteis que você pode usar com os comandos:

| **Comando** | **Flag** | **O que ela faz?**                                                                                   | **Exemplo**                                      |
|-------------|----------|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| `ls`        | `-l`     | Mostra uma lista detalhada com informações completas.                                               | `ls -l`                                          |
| `ls`        | `-a`     | Inclui arquivos ocultos na listagem.                                                                | `ls -la`                                         |
| `ls`        | `-h`     | Exibe tamanhos em um formato legível (ex.: KB, MB).                                                 | `ls -lh`                                         |
| `cp`        | `-r`     | Copia diretórios e seu conteúdo de forma recursiva.                                                 | `cp -r pasta_origem pasta_destino`               |
| `cp`        | `-p`     | Preserva atributos como permissões e datas dos arquivos.                                            | `cp -p arquivo1 arquivo2`                        |
| `cp`        | `-v`     | Mostra detalhes do processo de cópia (modo verboso).                                                | `cp -v arquivo1 arquivo2`                        |
| `rm`        | `-r`     | Remove diretórios e tudo que estiver dentro, de forma recursiva.                                    | `rm -r pasta`                                    |
| `rm`        | `-f`     | Força a remoção sem pedir confirmação.                                                            | `rm -rf arquivo`                                 |
| `tar`       | `-c`     | Cria um novo arquivo tar.                                                                           | `tar -cvf arquivo.tar pasta`                     |
| `tar`       | `-x`     | Extrai arquivos de um tar.                                                                          | `tar -xvf arquivo.tar`                           |
| `tar`       | `-z`     | Compacta ou descompacta arquivos usando gzip.                                                       | `tar -czvf arquivo.tar.gz pasta`                 |
| `tar`       | `-v`     | Mostra detalhes do processo de criação ou extração (modo verboso).                                  | `tar -cvf arquivo.tar pasta`                     |
| `tar`       | `-f`     | Define o nome do arquivo tar.                                                                       | `tar -czvf arquivo.tar.gz pasta`                 |
| `grep`      | `-i`     | Não diferencia maiúsculas de minúsculas ao procurar.                                               | `grep -i 'texto' arquivo`                        |
| `grep`      | `-r`     | Pesquisa de forma recursiva em diretórios.                                                          | `grep -r 'texto' pasta`                          |
| `grep`      | `-n`     | Mostra o número das linhas onde o texto foi encontrado.                                           | `grep -n 'texto' arquivo`                        |
| `chmod`     | `+x`     | Adiciona permissão de execução sem mudar outras permissões.                                         | `chmod +x script.sh`                             |
| `chmod`     | `u`      | Aplica alterações somente para o dono do arquivo.                                                 | `chmod u+x arquivo`                              |
| `chmod`     | `g`      | Aplica alterações para o grupo do arquivo.                                                        | `chmod g+w arquivo`                              |
| `chmod`     | `o`      | Aplica alterações para outros usuários.                                                           | `chmod o-r arquivo`                              |
| `chmod`     | `a`      | Aplica alterações para todos (dono, grupo e outros).                                              | `chmod a+x arquivo`                              |

*Exemplos práticos:*
- Para listar todos os arquivos (inclusive ocultos) em detalhes:
  ```bash
  ls -la
  ```
- Para copiar uma pasta inteira preservando os atributos:
  ```bash
  cp -rp pasta_origem pasta_destino
  ```
- Para remover uma pasta com tudo dentro sem ser perguntado:
  ```bash
  rm -rf nome_diretorio
  ```

> **Atenção:** O comando `rm -rf` é muito poderoso. Use-o com cuidado!

---

## 4. Dicas e Truques para Produtividade

- **Auto-completar:**  
  Use a tecla `Tab` para completar comandos e nomes de arquivos automaticamente.
- **Histórico de Comandos:**  
  Use `history` ou `Ctrl + R` para procurar por comandos já usados.
- **Aliases Personalizados:**  
  Crie atalhos para comandos frequentes. Por exemplo, adicione a linha abaixo no seu arquivo `~/.bashrc` ou `~/.zshrc`:
  ```bash
  alias ll="ls -la"
  ```

> **Dica Extra:**  
> Quer organizar seus scripts e poder executá-los de qualquer lugar? Faça o seguinte:
> 1. Crie uma pasta para os seus scripts:
>    ```bash
>    mkdir -p ~/scripts
>    ```
> 2. Adicione essa pasta ao seu PATH. Abra seu arquivo de configuração (por exemplo, `~/.bashrc` para Bash ou `~/.zshrc` para Zsh) e adicione esta linha no final:
>    ```bash
>    export PATH="$PATH:~/scripts"
>    ```
> 3. Para aplicar as mudanças imediatamente, rode:
>    ```bash
>    source ~/.bashrc  # ou source ~/.zshrc
>    ```

---

## 5. 10 Scripts Indispensáveis para Programadores

Aqui você encontra uma coleção de scripts que vão te ajudar a automatizar tarefas e aumentar sua produtividade. Cada script vem com uma explicação simples para te ajudar a entender o que cada comando faz.

### 1. **backup.sh** – Backup Automático
```bash
#!/bin/bash
SOURCE="/home/seu_usuario/documentos"
DEST="/home/seu_usuario/backup"
rsync -av --delete "$SOURCE" "$DEST"
```
- **O que ele faz:**  
  - Usa o `rsync` para sincronizar arquivos entre dois diretórios.
  - `-a` (archive) preserva as permissões e timestamps.
  - `-v` (verbose) mostra o que está acontecendo.
  - `--delete` remove arquivos no destino que não existem na origem.
- **Para que serve:**  
  Mantém um backup atualizado dos seus documentos, garantindo que o destino seja uma cópia exata da origem.

### 2. **system_stats.sh** – Monitoramento de CPU, Memória e Disco (Zsh)
```zsh
#!/bin/zsh
echo "Uso de CPU:"
mpstat

echo "Uso de memória:"
free -h

echo "Uso de disco:"
df -h
```
- **O que ele faz:**  
  - `mpstat` mostra estatísticas da CPU.
  - `free -h` exibe o uso de memória de forma legível.
  - `df -h` mostra quanto espaço em disco está sendo usado.
- **Para que serve:**  
  É ótimo para ter uma visão rápida do desempenho do seu sistema e identificar possíveis gargalos.

### 3. **update.sh** – Atualização do Sistema
```bash
#!/bin/bash
sudo apt update && sudo apt upgrade -y && sudo apt autoremove -y
```
- **O que ele faz:**  
  - Atualiza a lista de pacotes (`apt update`).
  - Atualiza os pacotes instalados, confirmando automaticamente (`apt upgrade -y`).
  - Remove pacotes que não são mais necessários (`apt autoremove -y`).
- **Para que serve:**  
  Mantém o sistema sempre atualizado e limpo, sem precisar digitar vários comandos separadamente.

### 4. **service_status.sh** – Verificando o Status dos Serviços
```bash
#!/bin/bash
services=("nginx" "mysql")
for service in "${services[@]}"; do
    systemctl status $service --no-pager
done
```
- **O que ele faz:**  
  - Itera sobre uma lista de serviços (como `nginx` e `mysql`).
  - Usa `systemctl status` para mostrar o status de cada serviço, sem paginação.
- **Para que serve:**  
  É perfeito para verificar rapidamente se serviços importantes estão rodando corretamente.

### 5. **build_project.sh** – Compilação de Projetos em C/C++
```bash
#!/bin/bash
for file in *.c; do
    gcc "$file" -o "${file%.c}"
done
```
- **O que ele faz:**  
  - Percorre todos os arquivos com extensão `.c`.
  - Compila cada arquivo com `gcc`, criando um executável sem a extensão `.c`.
- **Para que serve:**  
  Automatiza a compilação de programas em C, poupando tempo na hora de construir seus projetos.

### 6. **start_server.sh** – Servidor HTTP Simples
```bash
#!/bin/bash
python3 -m http.server 8000
```
- **O que ele faz:**  
  - Inicia um servidor web simples na porta 8000 usando Python.
- **Para que serve:**  
  Ideal para testar rapidamente páginas web ou compartilhar arquivos localmente.

### 7. **cleanup.sh** – Limpeza de Arquivos Temporários
```bash
#!/bin/bash
sudo rm -rf /tmp/*
```
- **O que ele faz:**  
  - Remove todos os arquivos e pastas dentro do diretório `/tmp` de forma recursiva e forçada.
- **Para que serve:**  
  Ajuda a liberar espaço e manter o sistema limpo, mas use com muito cuidado!

### 8. **replace.sh** – Busca e Substituição em Arquivos
```bash
#!/bin/bash
find . -type f -name "*.txt" -exec sed -i 's/antigo/novo/g' {} +
```
- **O que ele faz:**  
  - Usa `find` para localizar todos os arquivos `.txt` no diretório atual.
  - Usa `sed` para substituir todas as ocorrências de "antigo" por "novo" em cada arquivo.
- **Para que serve:**  
  É muito útil para atualizar textos ou configurações em vários arquivos de uma vez.

### 9. **net_check.sh** – Verificação de Conexões de Rede
```bash
#!/bin/bash
netstat -tulnp
```
- **O que ele faz:**  
  - Mostra informações detalhadas sobre as conexões de rede, incluindo quais portas estão em uso.
- **Para que serve:**  
  Ajuda a diagnosticar problemas de rede e identificar quais serviços estão consumindo a conexão.

### 10. **tail_logs.sh** – Monitoramento de Logs em Tempo Real
```bash
#!/bin/bash
tail -f /var/log/syslog
```
- **O que ele faz:**  
  - Acompanha as últimas linhas do arquivo de log do sistema em tempo real.
- **Para que serve:**  
  Útil para monitorar continuamente eventos e identificar problemas conforme eles acontecem.

> **Dica:** Salve todos esses scripts na pasta `~/scripts` e adicione essa pasta ao seu PATH para que você possa executá-los de qualquer lugar sem precisar digitar o caminho completo.

---

## 6. Bash vs. Zsh: Diferenças, Instalação & Recomendações

### Principais Diferenças

- **Bash:**  
  - É o shell padrão na maioria das distribuições Linux.
  - Tem ótima documentação e é muito bom para scripts e automação.
  
- **Zsh:**  
  - Muito personalizável, com autocompletar avançado e suporte a plugins.
  - Oferece uma experiência mais interativa e visual (dê uma olhada no [Oh My Zsh](https://ohmyz.sh/)).

### Qual Escolher?
- **Para Iniciantes:**  
  O Bash é ótimo porque já vem instalado e é bem documentado.
- **Para Usuários Avançados:**  
  O Zsh pode oferecer recursos extras que tornam a experiência de uso mais rica.

### Como Instalar

#### Atualizando ou Instalando Bash
```bash
sudo apt update
sudo apt install --only-upgrade bash
```

#### Instalando Zsh
1. **Instale o Zsh:**
   ```bash
   sudo apt update
   sudo apt install zsh -y
   ```
2. **Altere o Shell Padrão:**
   ```bash
   chsh -s $(which zsh)
   ```
   > Reinicie o terminal para que a mudança tenha efeito.
3. **Instale o Oh My Zsh:**
   ```bash
   sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```

---

## 7. Criando Seu Próprio Script (Bash e Zsh)

Criar seus próprios scripts pode facilitar muito sua vida no Linux. Veja como fazer isso de forma simples:

### Passo a Passo

1. **Crie um Arquivo de Script:**  
   Abra seu editor favorito e crie um novo arquivo, por exemplo:
   ```bash
   nano meu_script.sh
   ```
2. **Adicione a Shebang:**  
   No início do arquivo, diga qual interpretador usar:
   - Para **Bash**:
     ```bash
     #!/bin/bash
     ```
   - Para **Zsh**:
     ```bash
     #!/bin/zsh
     ```
3. **Escreva o Código:**  
   Coloque os comandos que você quer executar. Por exemplo:
   ```bash
   #!/bin/bash
   # Script de Boas-Vindas
   echo "Olá, seja bem-vindo ao mundo dos scripts!"
   ```
   Ou para Zsh:
   ```zsh
   #!/bin/zsh
   # Script de Boas-Vindas com Zsh
   echo "Olá, seja bem-vindo ao mundo dos scripts com Zsh!"
   ```
4. **Salve e Saia:**  
   No `nano`, pressione `Ctrl+O` para salvar e `Ctrl+X` para sair.
5. **Torne o Script Executável:**
   ```bash
   chmod +x meu_script.sh
   ```
6. **Execute o Script:**
   ```bash
   ./meu_script.sh
   ```

### Dicas Extras

- **Comentários:**  
  Use o símbolo `#` para comentar seu código e explicar o que cada parte faz.
- **Variáveis e Controle de Fluxo:**  
  Use variáveis e estruturas como `if`, `for`, e `while` para tornar seus scripts dinâmicos.
- **Depuração:**  
  Use comandos como `echo` para imprimir mensagens e verificar se o script está funcionando como esperado.

---

## 8. Recursos Adicionais

🔗 **Links Úteis:**
- [Documentação Oficial do Ubuntu](https://ubuntu.com/tutorials)
- [Guia de Comandos Linux](https://linuxcommand.org/)
- [Oh My Zsh](https://ohmyz.sh/)
- [Awesome Shell](https://github.com/alebcay/awesome-shell)

---

## 9. Conclusão

🎉 **Parabéns!**  
Você agora tem uma base sólida para explorar o mundo do Linux no Ubuntu. Este guia abrange desde a instalação, passando pelos comandos básicos, até scripts avançados e dicas para melhorar sua produtividade.  
Se este repositório te ajudou, não se esqueça de dar uma ⭐ e compartilhar com seus amigos!
