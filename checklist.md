# CHECKLIST PARA DESENVOLVIMENTO DE APLICAÇÕES MAIS SEGURAS

Quanto mais preparado para a jornada de desenvolvimento você estiver, maior será o seu êxito e menor serão os impactos e correções necessárias. <br />
Um código de alta qualidade e segurança, aumenta o valor geral do produto, reduzindo os custos e facilitando as atualizações e a manutenção. </p>

# O QUE FAZER

### VALIDE AS ENTRADAS DE DADOS DA APLICAÇÃO
Garanta que não seja permitido inclusão de código Javascript em seus campos. Assim evitando o ataque Cross-Site Scripting (XSS). Para isso utilize a sanitização dos campos para que caracteres especiais, como ( /, <,>,”,+,., ‘ e ?) sejam removidos ou rejeitados.

Troque ou escape os caracteres-chave por entidades HTML, de forma que o conteúdo da variável seja sempre considerado texto e nunca uma tag ou parte de um script.

Valide as informações de todos os campos de um formulário também no servidor (backend), inclusive o tamanho e o tipo de dados dos campos. Independentemente de existir ou não uma validação no frontend utilizando Javascript.

### FILTRE E VALIDE PARÂMETROS NO SERVIDOR
Para rejeitar ou eliminar o risco de SQL Injection, filtre e valide dados na chegada das requisições.

### ATENÇÃO AO PERMITIR O UPLOAD DE ARQUIVOS
Valide o formato, tamanho e não exiba o caminho onde a imagem foi salva.

### MANIPULAÇÃO DE URL
Podemos receber dados não confiáveis que resulta no redirecionamento do usuário para um outro endereço qualquer, causando problemas como: Open Redirect, by-pass no controle de acesso da aplicação e phishing. Para evitar, valide a URL com relação ao formato e as fontes de origem dos dados que compõe a URL.
Caso a aplicação aceite URLs de terceiros ou fornecedores, implemente políticas de whitelist

### DADOS SENSÍVEIS
Não inclua senhas ou chaves no código fonte e nem versione dados sensíveis.
Seja criterioso nas permissões aos arquivos e diretórios.

### DEPENDÊNCIAS E PACOTES EXTERNOS
O desenvolvimento de aplicativos modernos depende muito de bibliotecas de terceiros, como npm, Maven, Gradle PyPI ou qualquer gerenciador de pacotes semelhante. Por esse motivo, é importante garantir que não haja vulnerabilidades conhecidas nessas dependências da sua aplicação.


### IMPLEMENTE EXCEÇÕES E LOGS DE SEGURANÇA 
Para que se possa ter conhecimento dos ataques que estão sendo feitos contra sua aplicação, mantenha uma rotina de logs e gerenciamento de exceções com o máximo de informações possíveis para identificar a origem dos ataques.
