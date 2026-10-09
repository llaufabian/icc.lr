# Sistema de Achados e Perdidos UFRPE: Documento de Requisitos
> Atividade prática de Levantamento de Requisitos (ICC / UFRPE).
> Atividade de prática: não é entregue e não vale nota.
## 1. Equipe
| Nome | Curso |
|------|-------|
| Matheus | Ciência da Computação |
| Giovanna | Ciência da Computação |
| Jânio | Ciência da Computação |
| Francielly | Ciência da Computação |
| Jamilly | Ciência da Computação |
| Laura | Ciência da Computação |

## Visão geral

**Problema:** Objetos perdidos no campus da UFRPE ficam espalhados entre portarias, secretarias e grupos de mensagem, e raramente voltam ao dono.

**Solução proposta:** Um sistema centralizado de Achados e Perdidos da UFRPE onde a comunidade acadêmica pode registrar itens encontrados e buscar por pertences perdidos, conectando os pontos de guarda aos donos.

**Escopo:** O sistema gerencia o registro, a busca e a notificação de itens perdidos e encontrados. O sistema não faz entregas ou transporte físico dos objetos.

---

## Atores (usuários do sistema)

* **Estudante:** Aluno com matrícula ativa, que precisa procurar objetos ou registrar perdas.
* **Servidor:** Professor ou técnico, que pode registrar perdas ou itens encontrados.
* **Ponto de guarda:** Portaria, biblioteca ou secretaria que guarda o objeto fisicamente no campus.
* **Administrador:** Responsável por gerenciar as categorias da plataforma, moderar registros e lidar com itens expirados.

---

## Requisitos funcionais

| Código | Nome | Descrição | Ator(es) | Prioridade | Critérios de Aceitação |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF01** | Cadastrar objeto encontrado | O sistema deve permitir registrar um objeto encontrado, informando categoria, descrição, cor, local, data e foto opcional. | Estudante, Servidor, Ponto de guarda | Alta | 1. O formulário deve conter os campos listados.<br>2. O upload de foto deve ser opcional.<br>3. Se for documento (RN01), o sistema deve bloquear upload de foto.<br>4. O sistema deve exibir mensagem de sucesso ao salvar. |
| **RF02** | Buscar objetos | O sistema deve permitir buscar objetos por palavra-chave e filtrar por categoria, campus/local e período. | Estudante, Servidor, Ponto de guarda | Alta | 1. A busca deve possuir barra de texto e filtros dropdown.<br>2. Os resultados devem respeitar a privacidade de documentos (RN01).<br>3. Itens marcados como "Entregue" não devem aparecer na busca pública. |
| **RF03** | Registrar objeto perdido | Permitir que o usuário detalhe um item que perdeu no campus para criar um alerta de busca. | Estudante, Servidor | Alta | 1. O formulário deve exigir descrição, categoria e local provável.<br>2. O status inicial do registro deve ser "Perdido". |
| **RF04** | Solicitar devolução (reivindicar objeto) | O sistema deve permitir que o pretenso dono comprove a propriedade do objeto encontrado. | Estudante, Servidor | Alta | 1. O usuário deve poder enviar um texto com detalhes ocultos do item ou anexar um comprovante/foto.<br>2. O Ponto de guarda deve receber a notificação da solicitação.<br>3. O status do item deve mudar para "Em Análise". |
| **RF05** | Notificar possível correspondência | Avisar quem perdeu quando surgir um objeto com características semelhantes cadastrado na plataforma. | Sistema | Média | 1. O sistema deve cruzar dados de categoria, cor e local.<br>2. O usuário deve receber um alerta no sistema ou por e-mail com o link do objeto suspeito. |
| **RF06** | Registrar entrega ao dono | Confirmar a devolução final do item e retirá-lo da busca ativa. | Ponto de guarda | Alta | 1. Apenas o Ponto de guarda responsável pode executar esta ação (RN04).<br>2. O sistema deve exigir confirmação do documento validado (RN03).<br>3. O status do item deve mudar para "Entregue" e sair da listagem pública. |
| **RF07** | Autenticar usuário | Garantir que a plataforma seja logada com credenciais seguras. | Todos | Alta | 1. O usuário não logado não pode cadastrar ou reivindicar itens.<br>2. O login deve exigir e-mail institucional e senha mascarada/criptografada. |
| **RF08** | Gerenciar prazos de doação | Emitir relatórios para os pontos de guarda sobre itens não reclamados que atingiram o prazo limite de armazenamento. | Administrador, Ponto de guarda | Média | 1. O sistema deve sinalizar itens com mais de 90 dias de cadastro (RN02).<br>2. Deve ser possível exportar a lista de itens expirados.<br>3. O sistema deve permitir a alteração do status desses itens para "Doado" ou "Descartado". |

---

## Requisitos não funcionais

* **RNF01 (Usabilidade):** O sistema deve funcionar adequadamente em celular e computador, sendo testado em telas de 360 px a 1920 px.
* **RNF02 (Desempenho):** A busca deve responder rápido, entregando o resultado em até 2 segundos.
* **RNF03 (Segurança):** O banco de dados deve proteger as credenciais de acesso e os comprovantes de propriedade submetidos.
* **RNF04 (Privacidade/LGPD):** Não exibir dados pessoais de terceiros na interface pública.
* **RNF05 (Acessibilidade):** A interface deve ser compatível com diretrizes básicas de acessibilidade web.
* **RNF06 (Disponibilidade):** A plataforma deve permanecer online com alta taxa de uptime.

---

## Regras de negócio

* **RN01:** Documentos oficiais (RG, CNH, cartão) não têm foto publicada; aparecem só como "documento encontrado".
* **RN02:** Objetos não retirados em 90 dias são destinados para doação ou descartados.
* **RN03:** A retirada física exige a apresentação de documento com foto ou a confirmação de detalhes específicos do objeto.
* **RN04:** A alteração do status final para "Entregue" só pode ser realizada pelo Ponto de guarda que armazenou o item.

---

## Histórias de usuário

* **Como** estudante, **quero** buscar meu casaco pela cor e pelo local, **para** saber se alguém o encontrou sem ir a todas as portarias.
* **Como** vigilante da portaria, **quero** registrar rapidamente um item deixado comigo, **para** manter o controle do posto sem prejudicar a fiscalização do acesso.
* **Como** aluno que perdeu um item, **quero** receber um alerta caso um objeto com as características do meu seja encontrado, **para** recuperá-lo com agilidade.

---

## Dúvidas em aberto

* Quem pode acessar a aplicação: será restrito apenas à comunidade UFRPE ou o público em geral poderá visualizar os itens?
* Os objetos ficarão guardados centralizados em um só lugar ou permanecerão em vários pontos de coleta pelo campus?
* Qual será o protocolo de validação se dois usuários reivindicarem a propriedade do mesmo objeto genérico?