# Instalação do Bodhi Linux Legacy no VirtualBox

## 1. Introdução

Este documento apresenta o passo a passo para realizar o download, configurar, instalar e iniciar o **Bodhi Linux Legacy** utilizando o **Oracle VM VirtualBox**.

O Bodhi Linux é uma distribuição Linux leve, baseada em Ubuntu, que utiliza o ambiente gráfico **Moksha**. A versão **Legacy** é destinada a computadores com arquitetura de **32 bits (x86)** e possui requisitos de hardware reduzidos.

O objetivo deste procedimento é instalar o sistema operacional em uma máquina virtual, sem modificar ou substituir o sistema operacional principal do computador.

---

## 2. Requisitos

Antes de iniciar, é necessário possuir:

* Computador com Windows, Linux ou outro sistema compatível com o VirtualBox;
* Oracle VM VirtualBox instalado;
* Conexão com a Internet;
* Arquivo ISO do Bodhi Linux Legacy;
* Espaço disponível no armazenamento do computador;
* Memória RAM disponível para a máquina virtual.

### Requisitos mínimos do Bodhi Linux

De acordo com a documentação oficial do Bodhi Linux, os requisitos mínimos são:

| Recurso       | Requisito mínimo |
| ------------- | ---------------: |
| Processador   |          500 MHz |
| Arquitetura   |          32 bits |
| Memória RAM   |           512 MB |
| Armazenamento |             5 GB |

O próprio projeto recomenda mais de 512 MB de RAM para que o instalador funcione de maneira mais confortável.

---

# 3. Download do Bodhi Linux Legacy

## 3.1 Acessando o site oficial

O primeiro passo é acessar a página oficial de downloads do Bodhi Linux:

**Bodhi Linux – Downloads**

https://www.bodhilinux.com/download/

Na página de downloads, procure pela opção:

**Legacy Release (32-bit only)**

A versão Legacy possui aproximadamente **747 MB** e é uma versão de 32 bits.

---

## 3.2 Baixando a imagem ISO

Clique em:

**Download**

na seção **Legacy Release (32-bit only)**.

O arquivo baixado será uma imagem no formato:

```text
.iso
```

A ISO é a imagem do sistema operacional que será utilizada pelo VirtualBox para realizar a instalação.

Salve o arquivo em uma pasta de fácil acesso, por exemplo:

```text
Downloads
```

---

# 4. Verificação da ISO

É recomendado verificar a integridade do arquivo baixado antes da instalação.

O site oficial do Bodhi Linux disponibiliza arquivos de verificação, como **MD5** e **SHA256**, juntamente com os downloads.

No Windows, por exemplo, é possível utilizar o PowerShell:

```powershell
Get-FileHash "C:\Users\SeuUsuario\Downloads\arquivo.iso" -Algorithm SHA256
```

O resultado pode ser comparado com o valor SHA256 disponibilizado pelo Bodhi Linux.

Essa etapa é recomendada porque permite verificar se a imagem ISO foi baixada corretamente.

---

# 5. Criando a máquina virtual no VirtualBox

## 5.1 Abrindo o VirtualBox

Abra o:

**Oracle VM VirtualBox**

Na tela principal, clique em:

**Novo**

O VirtualBox possui um assistente para criação de máquinas virtuais, permitindo definir o nome, ISO, memória, processadores e armazenamento da máquina virtual.

---

# 6. Configurando a máquina virtual

## 6.1 Nome e sistema operacional

Na tela de criação da máquina virtual, utilize configurações semelhantes às seguintes:

| Configuração | Valor                             |
| ------------ | --------------------------------- |
| Nome         | Bodhi Linux Legacy                |
| Tipo         | Linux                             |
| Versão       | Other Linux (32-bit)              |
| ISO          | Arquivo ISO do Bodhi Linux Legacy |

Caso o VirtualBox reconheça automaticamente a ISO, confirme se a arquitetura selecionada está correta.

Como a versão Legacy é **32 bits**, não é necessário selecionar uma versão Linux de 64 bits.

---

## 6.2 Instalação automática

Se o VirtualBox apresentar a opção de instalação automática, é recomendado desmarcar:

```text
Skip Unattended Installation
```

Isso permite realizar a instalação manualmente e acompanhar todas as etapas do processo.

O VirtualBox permite selecionar uma ISO e iniciar a instalação automaticamente, mas também permite desativar a instalação automática para que o usuário realize o procedimento manualmente.

---

# 7. Configuração da memória RAM

Para uma máquina virtual destinada ao Bodhi Linux Legacy, uma configuração adequada para testes é:

```text
RAM: 1024 MB
```

ou:

```text
RAM: 1 GB
```

Embora o requisito mínimo seja 512 MB, utilizar 1 GB proporciona uma experiência mais confortável durante a instalação e utilização do sistema.

---

# 8. Configuração do processador

Na configuração de processadores, pode ser utilizado:

```text
1 processador
```

Como a versão Legacy é uma distribuição bastante leve, um processador virtual é suficiente para uma máquina virtual destinada a estudos.

O VirtualBox recomenda não atribuir à máquina virtual mais da metade dos threads de processamento disponíveis no computador hospedeiro.

---

# 9. Criação do disco virtual

Na etapa de armazenamento, selecione:

```text
Create a Virtual Hard Disk Now
```

Utilize, por exemplo:

```text
Tamanho: 10 GB
```

O requisito mínimo informado pelo Bodhi Linux é de 5 GB, portanto 10 GB oferece uma margem maior para a instalação e utilização do sistema.

### Tipo de disco

Pode ser utilizado:

```text
VDI (VirtualBox Disk Image)
```

### Armazenamento

Selecione:

```text
Dynamically allocated
```

O armazenamento dinâmico permite que o arquivo do disco virtual aumente conforme o espaço for utilizado.

---

# 10. Resumo da configuração

Uma configuração recomendada para esta atividade é:

| Item          | Configuração       |
| ------------- | ------------------ |
| Nome          | Bodhi Linux Legacy |
| Sistema       | Linux              |
| Arquitetura   | 32 bits            |
| Memória RAM   | 1024 MB            |
| Processadores | 1                  |
| Disco virtual | 10 GB              |
| Tipo do disco | VDI                |
| Alocação      | Dinâmica           |
| ISO           | Bodhi Linux Legacy |

---

# 11. Iniciando a máquina virtual

Depois de criar a máquina virtual:

1. Selecione **Bodhi Linux Legacy** no VirtualBox;
2. Clique em **Iniciar**;
3. A máquina virtual será aberta;
4. O VirtualBox iniciará utilizando a imagem ISO configurada.

O VirtualBox permite iniciar uma máquina virtual selecionando-a no gerenciador e clicando em **Start/Iniciar**.

---

# 12. Inicialização do Bodhi Linux

Após iniciar a máquina virtual, aparecerá a tela de inicialização do Bodhi Linux.

A distribuição possui um ambiente **Live**, permitindo iniciar o sistema antes de realizar a instalação definitiva. A documentação oficial informa que o ambiente Live pode ser utilizado para testar o sistema antes da instalação.

Selecione a opção para iniciar o Bodhi Linux.

A máquina virtual deverá carregar o sistema e apresentar o ambiente gráfico **Moksha**.

---

# 13. Iniciando a instalação

Depois que o Bodhi Linux iniciar, localize o instalador.

No ambiente gráfico, procure pela opção:

```text
Install Bodhi Linux
```

ou pelo ícone correspondente ao instalador.

Clique nele para iniciar o processo de instalação.

---

# 14. Configuração do idioma

Na primeira etapa do instalador, selecione o idioma desejado.

Para esta documentação, pode ser utilizado:

```text
Português (Brasil)
```

Depois clique em:

```text
Continuar
```

---

# 15. Configuração do teclado

Selecione o layout correspondente ao teclado utilizado.

Para um teclado brasileiro, normalmente pode ser selecionado:

```text
Português (Brasil)
```

É possível testar a configuração digitando alguns caracteres no campo disponibilizado pelo instalador.

Depois clique em:

```text
Continuar
```

---

# 16. Preparação para a instalação

O instalador poderá apresentar algumas opções relacionadas à conexão com a Internet e atualizações.

Como a instalação está sendo realizada em uma máquina virtual para fins acadêmicos, pode-se manter as opções padrão.

Depois, avance para a próxima etapa.

---

# 17. Particionamento do disco

Como o Bodhi Linux está sendo instalado em um **disco virtual criado exclusivamente para a máquina virtual**, pode ser utilizada a opção de apagar o disco virtual e instalar o sistema.

**Atenção:** essa opção apaga o conteúdo do disco selecionado.

Neste caso, o disco é o disco virtual de aproximadamente 10 GB criado anteriormente no VirtualBox, e não o disco físico principal do computador.

Selecione a opção equivalente a:

```text
Erase disk and install Bodhi Linux
```

Depois clique em:

```text
Install Now
```

---

# 18. Configuração do fuso horário

Selecione o fuso horário correspondente à sua localização.

Para o Brasil, selecione uma cidade da região correspondente ao seu fuso, por exemplo:

```text
São Paulo
```

Depois avance.

---

# 19. Criação do usuário

O instalador solicitará informações para criar o usuário.

Exemplo:

```text
Nome: Usuário
Nome do computador: bodhi-virtualbox
Nome de usuário: usuario
Senha: ********
```

Escolha uma senha que você consiga lembrar.

A conta criada será utilizada para acessar o sistema depois da instalação.

---

# 20. Início da instalação

Depois de confirmar todas as configurações, o instalador começará a copiar os arquivos para o disco virtual.

Durante essa etapa serão realizadas tarefas como:

* Cópia dos arquivos do sistema;
* Instalação dos componentes do Bodhi Linux;
* Configuração do sistema;
* Instalação do carregador de inicialização;
* Criação do usuário;
* Configuração inicial.

Aguarde o término do processo.

---

# 21. Reinicialização

Quando a instalação terminar, o instalador solicitará a reinicialização da máquina.

Selecione:

```text
Restart Now
```

Caso o VirtualBox continue inicializando pela ISO, será necessário remover/desmontar a ISO da unidade óptica virtual.

No VirtualBox:

```text
Dispositivos
→ Unidades Ópticas
→ Remover disco da unidade virtual
```

Depois reinicie a máquina virtual.

---

# 22. Primeiro início do Bodhi Linux

Após remover a ISO, reinicie a máquina virtual.

O VirtualBox deverá iniciar o sistema a partir do disco virtual.

Será apresentada a tela de login do Bodhi Linux.

Digite:

```text
Usuário
Senha
```

Depois pressione:

```text
Enter
```

O ambiente gráfico **Moksha** será carregado.

---

# 23. Sistema instalado

Após o login, o Bodhi Linux estará funcionando dentro do VirtualBox.

A estrutura será semelhante a:

```text
Computador físico
│
└── VirtualBox
    │
    └── Bodhi Linux Legacy
        │
        ├── CPU virtual
        ├── RAM virtual
        ├── Disco virtual
        └── Bodhi Linux
            └── Ambiente gráfico Moksha
```

Dessa forma, o Bodhi Linux funciona como um computador independente dentro do computador principal.

---

# 24. Testando o sistema

Após iniciar o sistema, recomenda-se realizar alguns testes.

### Teste 1 – Área de trabalho

Verifique se o ambiente gráfico Moksha foi carregado corretamente.

### Teste 2 – Terminal

Abra o terminal e execute:

```bash
uname -a
```

Esse comando apresenta informações sobre o kernel utilizado.

### Teste 3 – Memória

Execute:

```bash
free -h
```

Esse comando apresenta informações sobre a memória RAM disponível.

### Teste 4 – Arquitetura

Execute:

```bash
uname -m
```

Como estamos utilizando o Bodhi Linux Legacy, o resultado esperado deverá indicar uma arquitetura de 32 bits, como:

```text
i686
```

---

# 25. Desligando a máquina virtual

Para desligar corretamente o Bodhi Linux, utilize a opção de desligamento do próprio sistema.

Outra possibilidade é selecionar no VirtualBox:

```text
Máquina
→ ACPI Shutdown
```

Evite simplesmente fechar a janela e selecionar o desligamento forçado, pois isso equivale a interromper a energia de um computador físico.

---

# 26. Iniciando novamente o Bodhi Linux

Depois que a instalação estiver concluída, não será necessário utilizar novamente a ISO.

Para iniciar o sistema:

1. Abra o VirtualBox;
2. Selecione **Bodhi Linux Legacy**;
3. Clique em **Iniciar**;
4. Aguarde o carregamento;
5. Digite o usuário e a senha;
6. O ambiente gráfico será iniciado.

---

# 27. Problemas comuns

## 27.1 A opção de 32 bits não aparece

Se o VirtualBox não apresentar opções de sistemas operacionais de 32 bits, pode ser necessário verificar se a virtualização está habilitada no computador.

Dependendo do processador, a tecnologia pode aparecer como:

```text
Intel VT-x
```

ou:

```text
AMD-V
```

Também pode ser necessário verificar as configurações de virtualização na BIOS/UEFI.

---

## 27.2 Tela preta durante a inicialização

Caso a máquina virtual apresente problemas gráficos, verifique as configurações de vídeo do VirtualBox.

Também é possível tentar iniciar o Bodhi utilizando uma opção de gráficos seguros, caso ela esteja disponível no menu de inicialização. A documentação do Bodhi recomenda o modo **Safe Graphics** quando há problemas com a inicialização gráfica.

---

## 27.3 Sistema muito lento

Caso o sistema esteja lento:

* Aumente a RAM para 1,5 GB ou 2 GB;
* Verifique se o computador hospedeiro possui memória disponível;
* Mantenha apenas 1 processador virtual inicialmente;
* Feche programas desnecessários no computador principal.

---

# 28. Conclusão

A instalação do **Bodhi Linux Legacy** no VirtualBox permite estudar uma distribuição Linux de baixo consumo de recursos sem modificar o sistema operacional instalado no computador físico.

O processo realizado neste documento foi:

```text
Download da ISO
       ↓
Verificação da ISO
       ↓
Criação da máquina virtual
       ↓
Configuração de RAM e CPU
       ↓
Criação do disco virtual
       ↓
Inicialização pela ISO
       ↓
Instalação do Bodhi Linux
       ↓
Remoção da ISO
       ↓
Reinicialização
       ↓
Login
       ↓
Bodhi Linux Legacy funcionando no VirtualBox
```

A configuração utilizada também é adequada para uma atividade acadêmica de **Sistemas Operacionais**, pois permite demonstrar conceitos como máquina virtual, sistema operacional convidado, disco virtual, memória virtualizada, inicialização e instalação de um sistema operacional.

---

# 29. Referências

* Bodhi Linux. **Download**. Disponível em: https://www.bodhilinux.com/download/
* Bodhi Linux. **Installation Instructions**. Disponível em: https://www.bodhilinux.com/w/installation-instructions/
* Bodhi Linux. **System Requirements**. Disponível em: https://www.bodhilinux.com/w/system-requirements/
* Oracle. **VirtualBox User Manual**. Disponível em: https://docs.oracle.com/en/virtualization/virtualbox/
