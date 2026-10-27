# Sistema_Bancario-Java

Projeto acadêmico de Programação Orientada a Objetos em Java, ainda incompleto.

> Apesar do nome do repositório e da pasta `SistemaBancario`, os fontes atuais modelam uma **biblioteca**: livros, empréstimos, reservas, clientes e administradores. Não há contas, saldo, depósitos ou saques implementados.

## Estrutura e leitura

Os arquivos estão em `SistemaBancario/src/`, sem declaração de pacote.

| Arquivo | Papel no código atual |
| --- | --- |
| `Usuario.java`, `Acesso.java` | Contrato de usuário e enumeração de perfis |
| `Cliente.java`, `Administrador.java` | Dados de usuários e métodos, em grande parte apenas esboçados |
| `Livro.java` | Dados do livro e consulta de disponibilidade |
| `Emprestimo.java`, `StatusEmprestimo.java` | Datas e estado do empréstimo |
| `Reserva.java`, `StatusReserva.java` | Livro reservado, data e estado da reserva |
| `Main.java` | Ponto de entrada vazio |

`SistemaBancario/SistemaBancario.iml` é uma configuração de módulo do IntelliJ IDEA; o JDK é herdado do ambiente.

## Estado e limitações

- `Cliente.java` usa `List` sem importar `java.util.List` e referencia a classe `Multa`, ausente no repositório. O conjunto atual não compila como está.
- Cadastro, consultas, devolução, renovação e relatórios têm métodos sem implementação.
- `calcularDiasAtraso()` retorna sempre zero; isso não representa uma regra de multa pronta.
- A redefinição de senha do cliente usa um valor fixo de exemplo.
- Não há interface de uso, persistência, configuração Maven/Gradle ou testes automatizados versionados.

## Como estudar

Comece pelo contrato `Usuario`, compare suas implementações e acompanhe as relações entre `Livro`, `Reserva` e `Emprestimo`. Observe a diferença entre uma assinatura de método e uma operação implementada.

Para trabalhar nos fontes, configure um JDK na IDE e marque `SistemaBancario/src` como pasta de fontes. A compilação completa depende de resolver as pendências descritas acima; executar o `Main` vazio não demonstra um sistema funcional.

Esta documentação descreve o estado encontrado, sem alterar o código ou renomear o projeto.
