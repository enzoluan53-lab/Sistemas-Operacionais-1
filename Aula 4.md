---

# 📘 Aula 04 – Estrutura e Arquitetura de Sistemas Operacionais

## 🧠 Visão Geral

A estrutura de um Sistema Operacional define como seus componentes são organizados e como interagem para gerenciar recursos do computador.

---

## 🧩 Componentes do Sistema Operacional

* **Kernel**: núcleo do sistema, responsável pelo controle dos recursos
* **Gerenciamento de Processos**: controle da execução de programas
* **Gerenciamento de Memória**: alocação e proteção da memória
* **Sistema de Arquivos**: organização e armazenamento de dados
* **Entrada/Saída (E/S)**: comunicação com dispositivos
* **Drivers**: permitem a interação com hardware específico

---

## ⚙️ Kernel – O Núcleo do Sistema

### Funções principais:

* Gerenciar processos e threads
* Controlar memória (física e virtual)
* Gerenciar dispositivos
* Fazer comunicação entre hardware e software
* Garantir segurança do sistema

---

## 🔐 Modos de Execução

* **Modo Usuário**:

  * Execução de aplicações comuns
  * Acesso limitado ao hardware

* **Modo Kernel**:

  * Acesso total ao sistema
  * Execução de funções críticas

* **System Call**:

  * Interface entre programas e o kernel

👉 Essa separação aumenta a **segurança e estabilidade** do sistema.

---

## 🔄 Processos

* Um **processo** é um programa em execução
* Possui:

  * Código (text)
  * Dados
  * Pilha (stack)
  * Registradores
  * Recursos (arquivos, etc.)

---

## 💾 Memória e Espaço de Endereçamento

* Cada processo possui seu próprio espaço de memória
* O SO gerencia:

  * Alocação
  * Proteção
  * Uso eficiente da memória

---

## 📁 Sistema de Arquivos

* Organiza os dados em estrutura hierárquica (pastas/diretórios)
* Facilita:

  * Armazenamento
  * Acesso
  * Gerenciamento de informações

---

## 🔌 Entrada/Saída e Drivers

### Exemplos de dispositivos:

* Teclado

* Mouse

* Disco

* Rede

* Impressora

* **Drivers**:

  * Fazem a comunicação entre o SO e o hardware
  * Abstraem a complexidade dos dispositivos

---

## 🔄 Reaproveitamento de Estrutura

* Muitos sistemas operacionais são baseados em outros já existentes
* Vantagens:

  * Redução de custos
  * Maior estabilidade
  * Reutilização de tecnologia
  * Suporte contínuo

### Exemplos:

* Raspberry Pi OS → baseado no Debian (Linux)
* Orbis OS (PS4) → baseado no FreeBSD

---

## 📝 Atividade

1. Pesquisar **5 sistemas operacionais** que derivam de outros
2. Fazer uma **tabela comparativa** entre eles
3. Organizar tudo em **arquivo Markdown (.md)**
4. Salvar no repositório da disciplina

---

## 📚 Referências

* Tanenbaum – Sistemas Operacionais Modernos
* Silberschatz – Fundamentos de SO
* Stallings – Conceitos e Projetos
* Documentações oficiais (Red Hat, Docker)

---
Perfeito 👍 então já vou te entregar a **atividade da Aula 04 pronta em .md**, no padrão que o professor pediu.

---

# 📝 Atividade – Aula 04 (Markdown)

## 📊 Sistemas Operacionais Baseados em Outros

| Sistema Operacional | Base              | Principais Diferenças                                                    |
| ------------------- | ----------------- | ------------------------------------------------------------------------ |
| Ubuntu              | Debian (Linux)    | Interface amigável, foco em usuários iniciantes, atualizações frequentes |
| Linux Mint          | Ubuntu (Linux)    | Interface mais leve e semelhante ao Windows, foco em usabilidade         |
| Android             | Linux Kernel      | Adaptado para dispositivos móveis, gerenciamento de energia e apps       |
| macOS               | UNIX (Darwin/BSD) | Integração com hardware Apple, interface gráfica refinada                |
| Orbis OS (PS4)      | FreeBSD           | Otimizado para jogos, sistema fechado e focado em desempenho             |

---

## 📌 Análise Comparativa

* A maioria dos sistemas modernos reutiliza estruturas já existentes
* Sistemas baseados em Linux são altamente adaptáveis
* Sistemas comerciais (macOS, PS4) são mais fechados e otimizados
* Sistemas móveis (Android) possuem foco em eficiência energética
* O reaproveitamento reduz custos e aumenta a estabilidade

---

## 🎯 Conclusão

O uso de sistemas base como Linux e UNIX permite o desenvolvimento de novos sistemas operacionais com mais rapidez, segurança e eficiência. Cada sistema adapta sua base para atender necessidades específicas, como desktops, dispositivos móveis ou consoles.

---




