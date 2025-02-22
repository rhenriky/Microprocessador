 ### Microprocessadores SAP e MIPS no Logisim Evolution ### 

 IFMT Engenharia da Computação 

Introdução

Este projeto implementa dois microprocessadores distintos, o SAP (Simple As Possible) e o MIPS (Microprocessor without Interlocked Pipeline Stages), utilizando o Logisim Evolution. O objetivo é demonstrar a arquitetura e o funcionamento desses processadores em um ambiente de simulação lógica.

Microprocessador SAP

Visão Geral

O SAP é um microprocessador educacional projetado para ilustrar os conceitos fundamentais de arquitetura de computadores. Ele é composto por um conjunto mínimo de componentes que permitem a execução de instruções básicas.

Componentes Principais

Unidade de Controle: Decodifica as instruções e gera os sinais de controle apropriados.

Unidade Lógica e Aritmética (ULA): Executa operações matemáticas e lógicas.

Registradores: Armazenam dados temporários.

Barramento: Facilita a comunicação entre os componentes.

Memória: Armazena as instruções e os dados do programa.

Clock: Controla a sincronização dos sinais e operações do processador.

Decodificador de Instruções: Identifica a operação a ser executada.

Instruções Implementadas

LOAD (Carregar dado na memória)

ADD (Somar valores)

SUB (Subtrair valores)

STORE (Armazenar dados)

JMP (Pular para um endereço específico)

JNZ (Pulo condicional se diferente de zero)

HLT (Parar a execução)

Microprocessador MIPS

Visão Geral

O MIPS é um processador baseado na arquitetura RISC (Reduced Instruction Set Computing), amplamente utilizado em sistemas embarcados e acadêmicos devido à sua simplicidade e eficiência.

Componentes Principais

Unidade de Controle: Gerencia a execução das instruções.

Banco de Registradores: Contém registradores de propósito geral.

Unidade Lógica e Aritmética (ULA): Executa operações matemáticas e lógicas.

Memória de Instruções: Armazena as instruções do programa.

Memória de Dados: Armazena os dados temporários do programa.

Multiplexadores: Direcionam sinais e dados para as operações corretas.

Extensor de Sinal: Ajusta tamanhos de dados quando necessário.

Instruções Implementadas

ADD (Soma entre registradores)

SUB (Subtração entre registradores)

AND (Operação lógica AND)

OR (Operação lógica OR)

XOR (Operação lógica XOR)

LW (Load Word - Carregar um valor da memória para um registrador)

SW (Store Word - Armazenar um valor na memória)

BEQ (Branch if Equal - Desvio condicional)

BNE (Branch if Not Equal - Desvio se diferente)

J (Jump - Pulo incondicional)

Implementação no Logisim Evolution

Ambos os processadores foram implementados no Logisim Evolution, um software de simulação de circuitos digitais. Foram utilizados componentes básicos como multiplexadores, decodificadores, registradores, ALU e memória RAM para simular a execução de instruções. O projeto contém arquivos .circ que representam os circuitos desenvolvidos.

Requisitos

Logisim Evolution instalado na máquina.

Conhecimento básico sobre circuitos digitais e arquitetura de computadores.

Como Executar

Baixe e instale o Logisim Evolution.

Abra o arquivo correspondente ao microprocessador desejado.

Execute a simulação passo a passo ou em modo contínuo para observar a execução das instruções.

Modifique as instruções na memória para testar diferentes operações.

Utilize o terminal de simulação para depuração e análise do funcionamento do processador.

Testes e Validação

Para garantir a funcionalidade correta dos processadores, foram realizados diversos testes com diferentes sequências de instruções. Cada teste foi verificado para confirmar que os valores nos registradores e a execução das operações estavam corretos.

Exemplos de Testes

Teste 1: Soma de dois valores (SAP)

LOAD A, 5

LOAD B, 3

ADD A, B

STORE C, A

HLT

Resultado esperado: O valor 8 armazenado no registrador C.

Teste 2: Loop condicional (MIPS)

ADDI $t0, $zero, 10

ADDI $t1, $zero, 0

LOOP: ADDI $t1, $t1, 1

BNE $t1, $t0, LOOP

HLT

Resultado esperado: O registrador $t1 incrementado até 10 antes da parada.

Conclusão

Este projeto demonstra como arquiteturas de microprocessadores podem ser modeladas e simuladas no Logisim Evolution. A implementação do SAP permite uma visão simplificada da execução de instruções, enquanto o MIPS apresenta uma abordagem mais avançada baseada na arquitetura RISC.

Referências

Albert Paul Malvino, Donald P. Leach - Digital Principles and Applications

David A. Patterson, John L. Hennessy - Computer Organization and Design: The Hardware/Software Interface

Mano, M. Morris - Computer System Architecture

