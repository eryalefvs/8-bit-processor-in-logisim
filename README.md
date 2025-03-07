# 🧮🖥 Simulador de Processador de 8 bits no Logisim

## Descrição do Projeto
Este projeto consiste em um simulador de processador desenvolvido para compreender o funcionamento interno de uma CPU, feito na matéria de Concepção Estruturada de Circuitos Integrados, 6º período. Ele apresenta uma representação visual dos componentes essenciais de um processador, incluindo registradores, barramentos, unidade lógica e aritmética (ALU), contador de programa, memória e outros elementos fundamentais. O objetivo é demonstrar como esses componentes interagem para buscar, decodificar e executar instruções.

## Componentes do Processador e Suas Funções

### **Program Counter (PC)**
O contador de programa é responsável por armazenar o endereço da próxima instrução a ser buscada na memória. Ele incrementa seu valor automaticamente após cada ciclo de busca, garantindo a execução sequencial do código.

### **Memory Address Register (MAR)**
O registrador de endereço de memória armazena o endereço da memória que está sendo acessado. Ele recebe o valor do PC quando uma instrução precisa ser buscada ou quando dados precisam ser carregados da memória para os registradores.

### **Memory Buffer Register (MBR)**
O registrador de buffer de memória armazena temporariamente os dados lidos ou escritos na memória RAM. Ele atua como um intermediário entre a memória e os outros componentes da CPU.

### **Instruction Register (IR)**
O registrador de instrução recebe a instrução buscada da memória e a armazena para ser decodificada e executada.

### **Unidade de Controle (Control Unit - CU)**
A unidade de controle é responsável por interpretar as instruções armazenadas no IR e gerar sinais de controle para coordenar a execução das operações dentro do processador.

### **Registradores A e B**
Esses registradores armazenam operandos temporários utilizados nas operações aritméticas e lógicas realizadas pela ALU.

### **Unidade Lógica e Aritmética (ALU)**
A ALU é responsável por realizar operações matemáticas (adição, subtração, multiplicação, divisão) e lógicas (AND, OR, NOT, XOR) entre os operandos armazenados nos registradores A e B.

### **Registrador de Saída**
Armazena os resultados das operações realizadas pela ALU antes de enviá-los para outros dispositivos ou para a memória.

### **Memória RAM**
A memória principal do sistema, onde as instruções e os dados são armazenados temporariamente durante a execução do programa.

### **Barramentos (Bus)**
Os barramentos são canais de comunicação que transportam dados, endereços e sinais de controle entre os componentes da CPU e a memória. Existem três tipos principais:
- **Barramento de Dados:** Transporta os dados entre a CPU e a memória ou dispositivos de entrada/saída.
- **Barramento de Endereço:** Transporta o endereço de memória dos dados/instruções a serem acessados.
- **Barramento de Controle:** Envia sinais de controle para coordenar a leitura e escrita de dados na memória e nos registradores.

## Fluxo de Execução no Processador
O processador segue um ciclo padrão de execução de instruções, conhecido como **ciclo de busca, decodificação e execução**:

1. **Busca da Instrução:** O contador de programa (PC) fornece o endereço da instrução a ser buscada, que é armazenada no MAR. A memória envia a instrução para o MBR, que a transfere para o IR.

2. **Decodificação:** A unidade de controle interpreta a instrução armazenada no IR e gera os sinais necessários para executá-la.

3. **Execução:** Se for uma operação aritmética ou lógica, a ALU realiza a operação utilizando os registradores A e B. Se for uma instrução de movimentação de dados, os valores são transferidos entre os registradores e a memória.

4. **Armazenamento do Resultado:** O resultado da execução é armazenado no registrador de saída ou em um local designado na memória.

5. **Incremento do PC:** O contador de programa é atualizado para apontar para a próxima instrução e o ciclo se repete.

## Conclusão
Este projeto fornece uma representação visual detalhada do funcionamento interno de um processador, permitindo compreender como os componentes interagem para executar instruções. Ele é útil para aprendizado acadêmico e para quem deseja aprofundar seus conhecimentos sobre arquitetura de computadores e design de CPUs.

