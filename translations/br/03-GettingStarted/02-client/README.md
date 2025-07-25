<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "2342baa570312086fc19edcf41320250",
  "translation_date": "2025-06-17T15:40:38+00:00",
  "source_file": "03-GettingStarted/02-client/README.md",
  "language_code": "br"
}
-->
No código anterior nós:

- Importamos as bibliotecas
- Criamos uma instância de um cliente e conectamos usando stdio como transporte.
- Listamos prompts, recursos e ferramentas e os invocamos todos.

Pronto, um cliente que pode se comunicar com um Servidor MCP.

Vamos dedicar um tempo na próxima seção de exercícios para analisar cada trecho de código e explicar o que está acontecendo.

## Exercício: Escrevendo um cliente

Como dito acima, vamos com calma explicando o código, e sinta-se à vontade para programar junto se quiser.

### -1- Importando as bibliotecas

Vamos importar as bibliotecas que precisamos, precisaremos de referências a um cliente e ao protocolo de transporte escolhido, stdio. stdio é um protocolo para coisas que rodam na sua máquina local. SSE é outro protocolo de transporte que mostraremos em capítulos futuros, mas essa é sua outra opção. Por enquanto, vamos continuar com stdio.

Vamos avançar para a instanciação.

### -2- Instanciando cliente e transporte

Precisamos criar uma instância do transporte e do nosso cliente:

### -3- Listando as funcionalidades do servidor

Agora, temos um cliente que pode se conectar caso o programa seja executado. No entanto, ele não lista suas funcionalidades, então vamos fazer isso agora:

Ótimo, agora capturamos todas as funcionalidades. A pergunta é: quando as usamos? Bem, este cliente é bem simples, no sentido de que precisaremos chamar explicitamente as funcionalidades quando quisermos. No próximo capítulo, criaremos um cliente mais avançado que terá acesso ao seu próprio modelo de linguagem grande, LLM. Por enquanto, vamos ver como invocar as funcionalidades no servidor:

### -4- Invocando funcionalidades

Para invocar as funcionalidades, precisamos garantir que especificamos os argumentos corretos e, em alguns casos, o nome do que estamos tentando invocar.

### -5- Executando o cliente

Para executar o cliente, digite o seguinte comando no terminal:

## Tarefa

Nesta tarefa, você usará o que aprendeu para criar um cliente, mas criará um cliente próprio.

Aqui está um servidor que você pode usar e que precisa ser chamado via seu código cliente. Veja se consegue adicionar mais funcionalidades ao servidor para torná-lo mais interessante.

## Solução

[Solução](./solution/README.md)

## Principais Aprendizados

Os principais aprendizados deste capítulo sobre clientes são:

- Podem ser usados tanto para descobrir quanto para invocar funcionalidades no servidor.
- Podem iniciar um servidor enquanto se iniciam (como neste capítulo), mas clientes também podem se conectar a servidores já em execução.
- São uma ótima forma de testar as capacidades do servidor, ao lado de alternativas como o Inspector, como descrito no capítulo anterior.

## Recursos Adicionais

- [Construindo clientes em MCP](https://modelcontextprotocol.io/quickstart/client)

## Exemplos

- [Calculadora em Java](../samples/java/calculator/README.md)
- [Calculadora em .Net](../../../../03-GettingStarted/samples/csharp)
- [Calculadora em JavaScript](../samples/javascript/README.md)
- [Calculadora em TypeScript](../samples/typescript/README.md)
- [Calculadora em Python](../../../../03-GettingStarted/samples/python)

## O que vem a seguir

- Próximo: [Criando um cliente com um LLM](/03-GettingStarted/03-llm-client/README.md)

**Aviso Legal**:  
Este documento foi traduzido utilizando o serviço de tradução por IA [Co-op Translator](https://github.com/Azure/co-op-translator). Embora nos esforcemos para garantir a precisão, esteja ciente de que traduções automáticas podem conter erros ou imprecisões. O documento original em seu idioma nativo deve ser considerado a fonte autorizada. Para informações críticas, recomenda-se tradução profissional humana. Não nos responsabilizamos por quaisquer mal-entendidos ou interpretações equivocadas decorrentes do uso desta tradução.