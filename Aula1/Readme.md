# Aula 01 - Introdução aos Sistemas Operacionais

## 📚 Apresentação da Disciplina
* **Objetivo:** Compreender a estrutura, funcionamento e os principais componentes de um Sistema Operacional (SO).
* **Foco:** Gerenciamento de processos, memória, sistemas de arquivos e entrada/saída (E/S).

---

## 🖥️ O que é um Sistema Operacional?
Um SO é um software que atua como **intermediário** entre o usuário e o hardware do computador. 

### Principais Funções:
1.  **Gerenciador de Recursos:** Organiza o uso da CPU, memória e dispositivos por diferentes programas.
2.  **Máquina Estendida (Abstração):** Esconde a complexidade do hardware, oferecendo uma interface mais simples para o programador e usuário.

### Estrutura de Camadas:
1.  **Hardware:** CPU, Memória, Dispositivos.
2.  **Kernel (Núcleo):** A parte principal do SO que interage direto com o hardware.
3.  **User Space:** Onde rodam as aplicações (Navegador, VS Code, etc).

---

## 🛠️ Evolução dos Sistemas Operacionais
* **Sistemas de Lote (Batch):** Processavam cartões perfurados em sequência, sem interação humana.
* **Multiprogramação:** Vários programas na memória ao mesmo tempo; enquanto um faz E/S, a CPU executa outro.
* **Tempo Compartilhado (Time-sharing):** Permite que vários usuários usem o sistema simultaneamente, alternando a CPU tão rápido que parece contínuo.

---

## 📝 Conceitos Fundamentais
* **Processo:** É um programa em execução. Possui seu próprio espaço de memória e recursos.
* **Chamadas de Sistema (System Calls):** A "ponte" que as aplicações usam para pedir serviços ao Kernel (ex: criar um arquivo ou ler dados da rede).
* **Shell:** O interpretador de comandos que permite ao usuário interagir com o SO.

---
> **Nota de Estudo:** Entender como o SO gerencia a memória e os processos é fundamental para o desenvolvimento de sistemas eficientes no 4º semestre de ADS.
