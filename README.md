
# Consulta de CEPs com API ViaCEP em Java

Este projeto em Java realiza buscas de endereços a partir de CEPs utilizando a API pública do [ViaCEP](https://viacep.com.br/). O usuário informa os CEPs via terminal, e os resultados são exibidos na tela e salvos em um arquivo `ceps.json`.

## 🚀 Funcionalidades

- Leitura de CEPs digitados pelo usuário
- Validação básica de entrada com opção de sair digitando "sair"
- Requisições HTTP usando `HttpClient` nativo do Java 11+
- Conversão de JSON para objetos usando Gson
- Salvamento dos dados buscados em arquivo `.json` com formatação

## 🛠 Tecnologias utilizadas

- Java 11+
- Gson (para manipulação de JSON)
- API ViaCEP (gratuita e pública)
- `HttpClient` (nativo desde o Java 11)

## 💻 Como executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repo.git
   ```
2. Compile e execute o projeto:
   - Com uma IDE como IntelliJ ou Eclipse, ou
   - Pelo terminal:
     ```bash
     javac Main.java ConectaViaCepApi.java CepRecord.java
     java Main
     ```

3. Digite os CEPs conforme solicitado no terminal.

4. Ao encerrar com `sair`, um arquivo `ceps.json` será gerado com todos os dados coletados.

## 🧪 Exemplo de uso

```
Digite um cep para busca (Somente números, ex: 00111111) ou 'sair' para encerrar:
01001000
{
  "cep": "01001-000",
  "logradouro": "Praça da Sé",
  "bairro": "Sé",
  "localidade": "São Paulo",
  "uf": "SP",
  ...
}
```

## 📂 Estrutura do projeto

```
├── Main.java                  # Classe principal com a lógica do programa
├── ConectaViaCepApi.java     # Responsável pela conexão com a API
├── CepRecord.java            # Record que representa o JSON retornado pela API
├── ceps.json                 # Arquivo gerado com as buscas
```

## 📌 Observações

- O programa não valida se o CEP possui exatamente 8 dígitos ou se é numérico.
- A API pode retornar erros se o CEP não existir ou estiver mal formatado.

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
