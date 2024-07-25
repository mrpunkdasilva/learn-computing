Threads são as fatias de processos do sistema, são "fios" criados para resolver um processo, assim é possível faze mais de uma tarefa. 

> Uma thread é uma unidade básica de utilização de CPU

Vamos imaginar um cenário, de uma loja:
```
┌───────────────────────────────────────────────┐
│                   Gerente                     │
│   ┌──────────┐   ┌──────────┐   ┌──────────┐  │
│   │  Caixa 1 │   │  Caixa 2 |   │  Caixa 3 │  |
│   └──────────┘   └──────────┘   └──────────┘  │
│     ▲     ▲         ▲     ▲         ▲     ▲   │
│     │     │         │     │         │     │   │
│ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐  │
│ │Atend.│ │Atend.│ │Atend.│ │Atend.│ │Atend.│  │
│ │  1   │ │  2   │ │  3   │ │  4   │ │  5   │  │
│ └──────┘ └──────┘ └──────┘ └──────┘ └──────┘  │
└───────────────────────────────────────────────┘
```

**Pense assim:**
- O Gerente é a  thread main (seria o "fio" principal);
- O Caixa 1, 2 e 3 são respectivamente os lugares de entradas de dados, onde os atendentes fazer o atendimento dos clientes elas sendo as threads secundarias;
- Atendente 1, 2, 3... eles são os recursos da CPU, ou mesmo podemos chamar de CPU  onde ela irá servir para atender o cliente e alocar ou não determinados recursos que foram pedidos;
- Cliente seria o usuario que entrou com algum dado que é passado para o sistema operacional que faz alguma chamada nas threads secundarias (atendentes) thread main (gerente);

**Funcionamento:**
- O Gerente **cria e genrencia** as threads secundarias (caixas).
- As caixas são as responsaveis por **escolher um dos atendentes para atender** os clientes, de modo que elas são **independentes** e veja que logo cada uma está trabalhando de modo **concorrente**, como se estivessem "disputando".
- Os atendentes são os recursos usados pela CPU, ou mesmo pode se dizer a CPU, para resolver a thread, ou seja, executar determinada tarefa.

```
┌───────────────────────────────────────────────┐
│                   Gerente                    │
│ ┌───────┐ ┌───────┐ ┌───────┐                │
│ │  Caixa│ │  Caixa│ │  Caixa│                │
│ │   1   │ │   2   │ │   3   │                │
│ └───────┘ └───────┘ └───────┘                │
│     │         │         │                    │
│ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐
│ │Atend. │ │Atend. │ │Atend. │ │Atend. │ │Atend. │
│ │   1   │ │   2   │ │   3   │ │   4   │ │   5   │
│ └───────┘ └───────┘ └───────┘ └───────┘ └───────┘
│     │      |            │                    │
│  ┌───┐   ┌───┐   ┌───┐  |                    │
│  │ 👥│   │ 👥│   │👥 │--|                    │
│  └───┘   └───┘   └───┘                       │
└───────────────────────────────────────────────┘

1. O Gerente cria as threads de Caixa (Caixa 1, Caixa 2, Caixa 3). ➡️

┌───────────────────────────────────────────────┐
│                   Gerente                    │
│ ┌───────┐ ┌───────┐ ┌───────┐                │
│ │▶️Caixa▶️│ │  Caixa│ │  Caixa│                │
│ │   1   │ │   2   │ │   3   │                │
│ └───────┘ └───────┘ └───────┘                │
│     │         │         │                    │
│ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐
│ │Atend. │ │Atend. │ │Atend. │ │Atend. │ │Atend. │
│ │▶️  1  ▶️│ │   2   │ │   3   │ │   4   │ │   5   │
│ └───────┘ └───────┘ └───────┘ └───────┘ └───────┘
│     │         │         │                    │
│  ┌───┐   ┌───┐   ┌───┐  |                    │
│  │▶️👥▶️│   👥 │    👥 │--|                    │
│  └───┘   └───┘   └───┘                       │
└───────────────────────────────────────────────┘

2. Um cliente chega e é direcionado para a Caixa 1. 👉

┌───────────────────────────────────────────────┐
│                   Gerente                    │
│ ┌───────┐ ┌───────┐ ┌───────┐                │
│ │▶️Caixa▶️│ │  Caixa│ │  Caixa│                │
│ │   1   │ │   2   │ │   3   │                │
│ └───────┘ └───────┘ └───────┘                │
│     │         │         │                    │
│ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐
│ │Atend. │ │Atend. │ │Atend. │ │Atend. │ │Atend. │
│ │▶️  1  ▶️│ │   2   │ │   3   │ │   4   │ │   5   │
│ └───────┘ └───────┘ └───────┘ └───────┘ └───────┘
│     │       |           │                     │
│  ┌───┐   ┌───┐   ┌───┐--|                     │
│  │▶️👥▶️│  │👥 │   │👥 │                        │
│  └───┘   └───┘   └───┘                        │
└───────────────────────────────────────────────┘

3. A Caixa 1 utiliza o Atendente 1 para processar as compras do cliente. 💼
```


> Tudo isso é gerenciado e orquestrado pelo Sistema Operacional.

Assim , as threads compartilham de algumas coisas em comum:
- Seção de **código**;
- seção de **dados**;
- Seção de outras coisas como **arquivos** e **sinais**;

Trazendo para o exemplo acima temos que o Gerente, caixa e atendente compartilham de:
- Seção de códigos de conduta, o código que define o que eles devem fazer e como deve ser feito;
- Seção de dados, tanto da loja como deles mesmos ou de clientes ou tarefas
- Seção  de arquivos ou mesmo utensilios da loja

Pórem, não é só isso, **as threads possuem** básicamente:
- ID da thread
- Conjunto de registradores;
- Uma pilha;
- Contador de programa;

```
┌───────────────────────────────────────────────────────────────┐
│                   Gerente 👨‍💼                 
│ ┌─────────┐ ┌──────────┐ ┌─────────┐              
│ │ Caixa 1 │ │ Caixa 2  │ │ Caixa 3 │               
│ │ 💻 📁 🔣│ │ 💻 📁 🔣 │ │ 💻 📁 🔣│             
│ │ ID 1    │ │ ID 2     │ │ ID 3     │              
│ │ ⚙️ ⏱️ 🧠 │ │ ⚙️ ⏱️ 🧠  │ │ ⚙️ ⏱️ 🧠  │               
│ └─────────┘ └──────────┘ └──────────┘              
│           🔄         🔄         🔄           
│ ┌─────────┐ ┌──────────┐ ┌──────────┐ ┌───────┐   ┌──────────┐
│ │Atend. 1 │ │Atend.  2 │ │Atend. 3   │ │Atend. 4│ │Atend. 5  │  
│ │ 💻 📁 🔣│ │ 💻 📁 🔣 │ │ 💻 📁 🔣│ │ 💻 📁 🔣│ │ 💻 📁 🔣 │
│ │ ID 1    │ │ ID 2     │ │ ID 3     │ │ ID 4    │ │ ID 5     │    
│ │⚙️ ⏱️ 🧠  │ │⚙️ ⏱️ 🧠   |  │ ⚙️ ⏱️ 🧠│ │ ⚙️ ⏱️ 🧠 │ │ ⚙️ ⏱️ 🧠  │
│ └─────────┘ └──────────┘ └─────────┘ └─────────┘  └──────────┘
│           🔄         🔄         🔄         
│  ┌───┐   ┌───┐   ┌───┐   ┌───┐   ┌───┐       
│  │ 👤│   │ 👤│   │ 👤│   │ 👤│   │ 👤│        
│  └───┘   └───┘   └───┘   └───┘   └───┘        
└──────────────────────────────────────────────────────────────────┘
Nesta representação, utilizei os seguintes elementos:
- 👨‍💼: Símbolo do Gerente
- 💻: Código (seção de código compartilhada)
- 📁: Dados (seção de dados compartilhada)
- 🔣: Arquivos e Sinais (seção de outros recursos compartilhados)
- ⚙️: Registradores
- ⏱️: Contador de programa
- 🧠: Pilha
- 👤: Clientes
- 🔄: Fluxo de execução (threads)
- ID: Identificador único de cada thread

1. O Gerente 👨‍💼 cria as threads de Caixa (Caixa 1, Caixa 2, Caixa 3), cada uma com seu próprio ID, conjunto de registradores, pilha, contador de programa, e compartilhando a seção de código, dados, arquivos e sinais.

2. Os Atendentes (Atend. 1, Atend. 2, Atend. 3, Atend. 4, Atend. 5) também são criados como threads, com as mesmas características de ID, registradores, pilha e contador, além de compartilharem a seção de código, dados, arquivos e sinais com o Gerente e as Caixas.

3. Os Clientes 👤 chegam e são atendidos pelas threads de Caixa e Atendentes, que compartilham os recursos necessários para processar as compras.
```

As threads em seu uso, ou seja a forma como os processos são construidos, podem ser divididos em dois tipos threads:
- **Singlethread**: é uma **única** **thread** em uso;
- **Multithread**: são **varias** **threads** que funcionam simultaneamente, de modo **paralelas**;

