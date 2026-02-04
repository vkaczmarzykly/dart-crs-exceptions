dart-crs-exceptions

📦 Exemplo de projeto em Dart para demonstrar tratamento de erros, exceções personalizadas e Null Safety.

Esse repositório acompanha o conteúdo do curso Dart: lidando com erros, exceções e null safety — onde você aprende a identificar e tratar situações excepcionais (erros e exceções), criar suas próprias classes de exceção e trabalhar com Null Safety de forma eficiente em aplicações Dart.

📌 Sobre

Esse projeto é uma aplicação Dart simples, usada para ilustrar conceitos fundamentais de tratamento de exceções e segurança de nulos (Null Safety). Ele serve como base para:

entender diferenças entre erros e exceções;

usar try, on, catch e finally para capturar exceções;

criar e lançar exceções personalizadas;

manusear valores potencialmente nulos com Null Safety;

estruturar um projeto Dart com pastas para lógica principal e testes.

O código é dividido em partes didáticas para mostrar como aplicar essas técnicas corretamente.

🧠 Conceitos abordados

✔️ Erros vs Exceções – o que são e quando usar;
✔️ Tratamento de exceções com blocos try/on/catch/finally;
✔️ Exceções personalizadas — classes que estendem Exception para capturar situações específicas da aplicação;
✔️ Null Safety — como o Dart lida com valores nulos e como evitar falhas em tempo de execução;
✔️ Boas práticas de código e organização de projeto.

🗂 Estrutura do projeto
dart-crs-exceptions/
├── bin/                   → Entrypoint da aplicação
├── lib/                   → Código principal e definições de classes/exceções
├── test/                  → Testes automatizados (opcional)
├── pubspec.yaml           → Configura dependências e metadados do pacote
├── README.md              → Documentação do projeto
└── analysis_options.yaml  → Regras de lint/estilo do Dart


📌 Exemplo de padrões utilizados:

throw para lançar uma exceção;

try { … } on MyException catch (e) { … } para capturar tipos específicos de exceções;

uso de construções Exception customizadas para dar significado a erros de negócio.

🛠️ Como usar
1. Clonar o repositório
git clone https://github.com/vkaczmarzykly/dart-crs-exceptions.git
cd dart-crs-exceptions

2. Instalar dependências
dart pub get

3. Rodar a aplicação
dart run


Dependendo do projeto, você verá mensagens no console representando operações do programa e como ele trata ou lança exceções.

🎯 Exemplos de código (genéricos)

Tratando exceções em Dart

try {
  // bloco de código que pode lançar exceções
} on FormatException catch (e) {
  print('Erro de formato: $e');
} catch (e) {
  print('Erro inesperado: $e');
} finally {
  print('Bloco finally sempre executa');
}


Criando exceção personalizada

class InvalidOperationException implements Exception {
  final String message;
  InvalidOperationException(this.message);

  @override
  String toString() => 'InvalidOperationException: $message';
}

🧪 Boas práticas

✔️ Trate exceções com tipos específicos quando possível (e não apenas catch (e) genérico).
✔️ Use Null Safety para evitar falhas inesperadas com valores nulos.
✔️ Separe lógica de negócios da lógica de tratamento de erros para manter o código limpo e testável.

📚 Recursos adicionais

Para aprofundar seu conhecimento em tratamento de exceções e Null Safety no Dart:

Curso completo na Alura: Dart: lidando com erros, exceções e null safety — com exemplos, exercícios e explicações passo a passo.

Documentação oficial Dart sobre Exception e tratamento de erros.

📝 Licença

Esse projeto segue a licença especificada em LICENSE (se houver), ou é fornecido “como está” para fins educacionais.
